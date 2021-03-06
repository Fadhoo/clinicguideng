<template>
  <div id="map"></div>
</template>

<script>
import stores from './stores.json'
export default {
    name: 'Locator',
    methods: {
        // Escapes HTML characters in a template literal string, to prevent XSS.
        // See https://www.owasp.org/index.php/XSS_%28Cross_Site_Scripting%29_Prevention_Cheat_Sheet#RULE_.231_-_HTML_Escape_Before_Inserting_Untrusted_Data_into_HTML_Element_Content
        sanitizeHTML(strings) {
        const entities = {'&': '&amp;', '<': '&lt;', '>': '&gt;', '"': '&quot;', '\'': '&#39;'};
        let result = strings[0];
        for (let i = 1; i < arguments.length; i++) {
            result += String(arguments[i]).replace(/[&<>'"]/g, (char) => {
            return entities[char];
            });
            result += strings[i];
        }
        return result;
        },
        /**
         * Initialize the Google Map.
         */
        /**
        * Use Distance Matrix API to calculate distance from origin to each store.
        * @param {google.maps.Data} data The geospatial data object layer for the map
        * @param {google.maps.LatLng} origin Geographical coordinates in latitude
        * and longitude
        * @return {Promise<object[]>} n Promise fulfilled by an array of objects with
        * a distanceText, distanceVal, and storeid property, sorted ascending
        * by distanceVal.
        */
        async calculateDistances(data, origin) {
            const stores = [];
            const destinations = [];

            // Build parallel arrays for the store IDs and destinations
            data.forEach((store) => {
                const storeNum = store.getProperty('storeid');
                const storeLoc = store.getGeometry().get();

                stores.push(storeNum);
                destinations.push(storeLoc);
            });

            // Retrieve the distances of each store from the origin
            // The returned list will be in the same order as the destinations list
            const service = new google.maps.DistanceMatrixService();
            const getDistanceMatrix =
                (service, parameters) => new Promise((resolve, reject) => {
                service.getDistanceMatrix(parameters, (response, status) => {
                    if (status != google.maps.DistanceMatrixStatus.OK) {
                    reject(response);
                    } else {
                    const distances = [];
                    const results = response.rows[0].elements;
                    for (let j = 0; j < results.length; j++) {
                        const element = results[j];
                        const distanceText = element.distance.text;
                        const distanceVal = element.distance.value;
                        const distanceObject = {
                        storeid: stores[j],
                        distanceText: distanceText,
                        distanceVal: distanceVal,
                        };
                        distances.push(distanceObject);
                    }

                    resolve(distances);
                    }
                });
                });

            const distancesList = await getDistanceMatrix(service, {
                origins: [origin],
                destinations: destinations,
                travelMode: 'DRIVING',
                unitSystem: google.maps.UnitSystem.METRIC,
            });

            distancesList.sort((first, second) => {
                return first.distanceVal - second.distanceVal;
            });

            return distancesList;
        },

        /**
        * Build the content of the side panel from the sorted list of stores
        * and display it.
        * @param {google.maps.Data} data The geospatial data object layer for the map
        * @param {object[]} stores An array of objects with a distanceText,
        * distanceVal, and storeid property.
        */
        showStoresList(data, stores) {
            if (stores.length == 0) {
                console.log('empty stores');
                return;
            }

            let panel = document.createElement('div');
            // If the panel already exists, use it. Else, create it and add to the page.
            if (document.getElementById('panel')) {
                panel = document.getElementById('panel');
                // If panel is already open, close it
                if (panel.classList.contains('open')) {
                panel.classList.remove('open');
                }
            } else {
                panel.setAttribute('id', 'panel');
                const body = document.body;
                body.insertBefore(panel, body.childNodes[0]);
            }


            // Clear the previous details
            while (panel.lastChild) {
                panel.removeChild(panel.lastChild);
            }

            stores.forEach((store) => {
                // Add store details with text formatting
                const name = document.createElement('p');
                name.classList.add('place');
                const currentStore = data.getFeatureById(store.storeid);
                name.textContent = currentStore.getProperty('name');
                panel.appendChild(name);
                const distanceText = document.createElement('p');
                distanceText.classList.add('distanceText');
                distanceText.textContent = store.distanceText;
                panel.appendChild(distanceText);
            });

            // Open the panel
            panel.classList.add('open');

            return;
        },
        initMap() {
            const mapStyle = [{
                'featureType': 'administrative',
                'elementType': 'all',
                'stylers': [{
                    'visibility': 'on',
                },
                {
                    'lightness': 33,
                },
                ],
                },
                {
                'featureType': 'landscape',
                'elementType': 'all',
                'stylers': [{
                    'color': '#f2e5d4',
                }],
                },
                {
                'featureType': 'poi.park',
                'elementType': 'geometry',
                'stylers': [{
                    'color': '#c5dac6',
                }],
                },
                {
                'featureType': 'poi.park',
                'elementType': 'labels',
                'stylers': [{
                    'visibility': 'on',
                },
                {
                    'lightness': 20,
                },
                ],
                },
                {
                'featureType': 'road',
                'elementType': 'all',
                'stylers': [{
                    'lightness': 20,
                }],
                },
                {
                'featureType': 'road.highway',
                'elementType': 'geometry',
                'stylers': [{
                    'color': '#c5c6c6',
                }],
                },
                {
                'featureType': 'road.arterial',
                'elementType': 'geometry',
                'stylers': [{
                    'color': '#e4d7c6',
                }],
                },
                {
                'featureType': 'road.local',
                'elementType': 'geometry',
                'stylers': [{
                    'color': '#fbfaf7',
                }],
                },
                {
                'featureType': 'water',
                'elementType': 'all',
                'stylers': [{
                    'visibility': 'on',
                },
                {
                    'color': '#acbcc9',
                },
                ],
            },
            ];
            // Create the map.
            const map = new google.maps.Map(document.getElementById('map'), {
                zoom: 7,
                center: {lat: 52.632469, lng: -1.689423},
                styles: mapStyle,
            });

            // Load the stores GeoJSON onto the map.
            map.data.loadGeoJson(stores, {idPropertyName: 'storeid'});

            // Define the custom marker icons, using the store's "category".
            map.data.setStyle((feature) => {
                return {
                icon: {
                    url: `img/icon_${feature.getProperty('category')}.png`,
                    scaledSize: new google.maps.Size(64, 64),
                },
                };
            });

            const apiKey = 'AIzaSyClaYOejMhAAJWhJ_7v1vb5k3hh8IKWEBw';
            const infoWindow = new google.maps.InfoWindow();

            // Show the information for a store when its marker is clicked.
            map.data.addListener('click', (event) => {
                const category = event.feature.getProperty('category');
                const name = event.feature.getProperty('name');
                const description = event.feature.getProperty('description');
                const hours = event.feature.getProperty('hours');
                const phone = event.feature.getProperty('phone');
                const position = event.feature.getGeometry().get();
                const content = sanitizeHTML`
                <img style="float:left; width:200px; margin-top:30px" src="img/logo_${category}.png">
                <div style="margin-left:220px; margin-bottom:20px;">
                    <h2>${name}</h2><p>${description}</p>
                    <p><b>Open:</b> ${hours}<br/><b>Phone:</b> ${phone}</p>
                    <p><img src="https://maps.googleapis.com/maps/api/streetview?size=350x120&location=${position.lat()},${position.lng()}&key=${apiKey}&solution_channel=GMP_codelabs_simplestorelocator_v1_a"></p>
                </div>
                `;

                infoWindow.setContent(content);
                infoWindow.setPosition(position);
                infoWindow.setOptions({pixelOffset: new google.maps.Size(0, -30)});
                infoWindow.open(map);
            });

            // Build and add the search bar
            const card = document.createElement('div');
            const titleBar = document.createElement('div');
            const title = document.createElement('div');
            const container = document.createElement('div');
            const input = document.createElement('input');
            const options = {
                types: ['address'],
                componentRestrictions: {country: 'gb'},
            };

            card.setAttribute('id', 'pac-card');
            title.setAttribute('id', 'title');
            title.textContent = 'Find the nearest store';
            titleBar.appendChild(title);
            container.setAttribute('id', 'pac-container');
            input.setAttribute('id', 'pac-input');
            input.setAttribute('type', 'text');
            input.setAttribute('placeholder', 'Enter an address');
            container.appendChild(input);
            card.appendChild(titleBar);
            card.appendChild(container);
            map.controls[google.maps.ControlPosition.TOP_RIGHT].push(card);

            // Make the search bar into a Places Autocomplete search bar and select
            // which detail fields should be returned about the place that
            // the user selects from the suggestions.
            const autocomplete = new google.maps.places.Autocomplete(input, options);

            autocomplete.setFields(
                ['address_components', 'geometry', 'name']);

            // Set the origin point when the user selects an address
            const originMarker = new google.maps.Marker({map: map});
            originMarker.setVisible(false);
            let originLocation = map.getCenter();

            autocomplete.addListener('place_changed', async () => {
                originMarker.setVisible(false);
                originLocation = map.getCenter();
                const place = autocomplete.getPlace();

                if (!place.geometry) {
                // User entered the name of a Place that was not suggested and
                // pressed the Enter key, or the Place Details request failed.
                window.alert('No address available for input: \'' + place.name + '\'');
                return;
                }

                // Recenter the map to the selected address
                originLocation = place.geometry.location;
                map.setCenter(originLocation);
                map.setZoom(9);
                console.log(place);

                originMarker.setPosition(originLocation);
                originMarker.setVisible(true);

                // Use the selected address as the origin to calculate distances
                // to each of the store locations
                const rankedStores = await calculateDistances(map.data, originLocation);
                showStoresList(map.data, rankedStores);

                return;
            });
        },
    },
    mounted(){
         /**
         * Initialize the Google Map.
         */
        this.initMap()

    }

}
</script>

<style scoped>
    #map {
      height: 100%;
    }
    
    html,
    body {
      height: 100%;
      margin: 0;
      padding: 0;
    }

    /* Styling for autocomplete search bar */
    #pac-card {
      background-color: #fff;
      border-radius: 2px 0 0 2px;
      box-shadow: 0 2px 6px rgba(0, 0, 0, 0.3);
      box-sizing: border-box;
      font-family: Roboto;
      margin: 10px 10px 0 0;
      -moz-box-sizing: border-box;
      outline: none;
    }
    
    #pac-container {
      padding-top: 12px;
      padding-bottom: 12px;
      margin-right: 12px;
    }
    
    #pac-input {
      background-color: #fff;
      font-family: Roboto;
      font-size: 15px;
      font-weight: 300;
      margin-left: 12px;
      padding: 0 11px 0 13px;
      text-overflow: ellipsis;
      width: 400px;
    }
    
    #pac-input:focus {
      border-color: #4d90fe;
    }
    
    #title {
      color: #fff;
      background-color: #acbcc9;
      font-size: 18px;
      font-weight: 400;
      padding: 6px 12px;
    }
    
    .hidden {
      display: none;
    }

    /* Styling for an info pane that slides out from the left. 
     * Hidden by default. */
    #panel {
      height: 100%;
      width: null;
      background-color: white;
      position: fixed;
      z-index: 1;
      overflow-x: hidden;
      transition: all .2s ease-out;
    }
    
    .open {
      width: 250px;
    }
    
    .place {
      font-family: 'open sans', arial, sans-serif;
      font-size: 1.2em;
      font-weight: 500;
      margin-block-end: 0px;
      padding-left: 18px;
      padding-right: 18px;
    }
    
    .distanceText {
      color: silver;
      font-family: 'open sans', arial, sans-serif;
      font-size: 1em;
      font-weight: 400;
      margin-block-start: 0.25em;
      padding-left: 18px;
      padding-right: 18px;
    }
</style>