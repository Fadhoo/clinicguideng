<template>
    <Navbar/>
    <body>
        <section class="justify-items-center max-w-7xl md:mx-auto px-4 pt-10">
            
            <div class="mapouter">

                <div style="width:100%;height:630px;">
                    <locator/>
                </div>
                
                <!-- <iframe
                width="100%"
                height="630px"
                id="gmap_canvas"
                src="https://maps.google.com/maps?q=%20Igbobi%20102216,%20Lagos&t=&z=13&ie=UTF8&iwloc=&output=embed"
                frameborder="0"
                scrolling="no"
                marginheight="0"
                marginwidth="0"
                ></iframe
                > -->
                
            </div>
            
        </section>
        <section class="justify-items-center max-w-7xl md:mx-auto px-4 pt-10">
            <div class="card flex p-10 justify-center ">
                <div class="w-full ">
                    <h3 class="text-white place-self-start" style="font-weight: 900; font-size: 42px;">Similar To Health Care Centers Near You:</h3>
                    <hr class="line">
                    <div class="grid bg-blue grid-cols-4 ">
                        <div class=" col-span-3 ">
                        <h4 class="hospital-name">Saint Mary’s Catholic Hosptial</h4>
                        <p class="address-name ">3.4 miles away</p>
                        </div>
                        <div>
                        <img class="pl-10 pt-5 justify-self-end" src="../assets/big_arrow.png" alt="arrow">
                        </div>
                    </div>
                    <hr class="line">
                    <div class="grid bg-blue grid-cols-4 ">
                        <div class=" col-span-3 ">
                        <h4 class="hospital-name">DayStar Hospital</h4>
                        <p class="address-name">4.2 miles away</p>
                        </div>
                        <div>
                        <img class="pl-10 pt-5 justify-self-end" src="../assets/big_arrow.png" alt="arrow">
                        </div>
                    </div>
                    <hr class="line">
                    <div class="grid bg-blue grid-cols-4 ">
                        <div class=" col-span-3 ">
                        <h4 class="hospital-name">Samaria Hospital</h4>
                        <p  class="address-name">5.8 miles away</p>
                        </div>
                        <div>
                        <img class="pl-10 pt-5 justify-self-end" src="../assets/big_arrow.png" alt="arrow">
                        </div>
                    </div>
                    <hr class="line">
                    <div class="grid bg-blue grid-cols-4 ">
                        <div class="col-span-3 ">
                        <h4 class="hospital-name">GetWell Hospital</h4>
                        <p  class="address-name text-sm">6 miles away</p>
                        </div>
                        <div>
                        <img class="pl-10 pt-5 justify-self-end" src="../assets/big_arrow.png" alt="arrow">
                        </div>
                    </div>
                    <hr class="line">
                </div>
            </div>
            
        </section>
        <section class="justify-center max-w-7xl bottom-0  md:mx-auto px-4 pt-20">
            <div class="bg-white shadow">
            <div class="justify content-center">
                <p class="clinicblue text-center">
                © 2021 Copyright:
                <a
                href="#"
                class="clinicblue"
                >Clinic Guide NG. All rights reserved.</a
                >
                </p>
            
            </div>
            </div>
        </section>
    </body>
    
</template>

<script>
// @ is an alias to /src
import Navbar from '@/components/Navbar.vue'
import Locator from '@/components/Locator.vue'

export default {
    components: {
        Navbar,
        Locator,
    }

}
</script>

<style scoped>
.hospital-name{
    font-size: 35px;
    color: white;
    font-weight: 700;
    text-align: center;
}

.address-name{
    color: white;
    font-size: 21px;
    font-weight: bold;
    text-align: center;
}
.line {
    width: 980px;
    margin: auto;
}

.card-style {
    width: 1196px;
    height: 630px;
}
</style>