<template>
  <PlaceSearch
    v-bind:ready="ready"
    placeholder="Enter a location"
    loading="Map is loading"
    v-bind:fallbackProcedure="fallbackProcedure"
    v-bind:zoom="zoom"
    v-bind:geolocation="geolocation"
    v-bind:gps_timeout="3000"
    v-bind:address="address"
    @changed="getMapData"
    >
  </PlaceSearch>

</template>

<script>
export default {
  name: "Locator",
  data() {
    return {
      ready: true, //Add ready:false to stop map from loading, and then when changed to true map will auto load
      // **GPS** : will trigger geolocation plugin , to find users location by GPS
      // **geolocation** : will try to find the place by lat, lng
      // **address**: will try to find the place by address query
      // **manually**: manually preset values

      // If GPS is selected as a fallbackProcedure and it fails , then address fallback is triggered and if address fails geolocation is triggered
      fallbackProcedure: "gps", //gps | geolocation | address | manually
      zoom: 17, //Default Zoom
      geolocation: {
        // If GPS and Find by address fails then, map will be positioned by a default geolocation
        lat: 31.73858,
        lng: -35.98628,
        zoom: 2,
      },
      address: {
        query: "Albania, Tirane", //If GPS fails, Find by address is triggered
        zoom: 10,
      },
      manually: {
        address_description: "21 Dhjetori, Tirana, Albania",
        city: "Tirana",
        country: "Albania",
        lat: 41.3267905,
        lng: 19.8060475,
        state: "Tirana County",
        zip_code: "",
        zoom: 17,
      },
      place: {},
    };
  },
  methods: {
    getMapData(place) {
      this.place = place;
    },
  },
  created() {},
};
</script>

<style>

</style>