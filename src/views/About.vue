<template>
  <Navbar/>
  <section class="max-w-7xl md:mx-auto px-4 pt-20">
    <div class="grid bg-blue lg:grid-cols-2 md:grid-cols-1 place-items-center">
      <div class="box">
        <img class="m-auto" src="../assets/wheel.png" alt="wheel">
        <br>
        <h3 class="box-title text-center">Our Vision</h3>
        <p class="title-tag text-center">For Nigerians around the country to have unbridled access to healthcare wherever they are in the country.</p>
      </div>
      <div class="box">
        <img class="m-auto" src="../assets/hill.png" alt="hill">
        <br>
        <h3 class="box-title text-center">Our Mission</h3>
        <p class="title-tag text-center">To connect Nigerians with credible hospitals in Nigeria by providing the most helpful, trusted information available.</p>
      </div>
    </div>
  </section>
  <section class="max-w-7xl md:mx-auto px-4 pt-20">
    <div class="container justify-center">
      <div class="grid sm:grid-rows-3 lg:grid-rows-none lg:grid-cols-3 " style="">
        <div class="z-20 ">
          <h3 style="font-size: 56px; font-weight: 900; color: #002366;">What Our <br> Users Say</h3>
          <img class="lg:ml-10 z-20" src="../assets/girl.png" alt="">
          <div class="grid grid-cols-2 mt-1">
            <img class="place-self-end pb-2" src="../assets/arrow-left.png" alt="">
            <img src="../assets/arrow-right.png" alt="" class="place-self-start">
          </div>
        </div>
        
        
        <div class="lg:col-span-2 lg:max-w-full card" style="height: 630px; max-width: 720px;">
          <h3 class="box-title text-right text-white mt-10 mr-10 ">Came Through <br> In An Emergency</h3>
          <p class="text-white text-right mt-10 mr-10" style="font-size: 28px; font-weight: 500;">
            Clinic Guide helped me find a nearby clinic <br>
            to get my brother an inhaler who was having <br>
            an asthma attack.
          </p>
          <h3 class="text mt-20 ml-20 text-left font-bold">Adesuwa</h3>
          <p class="text mt-2 ml-20 text-left">Idumota, Lagos</p>
           
        </div>
      </div>
        
    </div>
  </section>
  <section class="pt-20">
    <div class="bigger-card">
      <div class="grid lg:grid-cols-4 md:grid-cols-1">
        <div class="container p-20">
          <img src="../assets/rect.png" alt="">
          <h3 class="text-white name-tag">
            Dr Adeola Olatunji
          </h3>
          <p class="text-white title-tag">CEO, ClinicGuideNG</p>
          <img src="../assets/linkedin.png" alt="">
        </div>

        <div class="container p-20">
          <img src="../assets/rect.png" alt="">
          <h3 class="text-white name-tag">
            Dr Adeola Olatunji
          </h3>
          <p class="text-white title-tag">CEO, ClinicGuideNG</p>
          <img src="../assets/linkedin.png" alt="">
        </div>

        <div class="container p-20">
          <img src="../assets/rect.png" alt="">
          <h3 class="text-white name-tag">
            Dr Adeola Olatunji
          </h3>
          <p class="text-white title-tag">CEO, ClinicGuideNG</p>
          <img src="../assets/linkedin.png" alt="">
        </div>

        <div class="container p-20">
          <img src="../assets/rect.png" alt="">
          <h3 class="text-white name-tag">
            Dr Adeola Olatunji
          </h3>
          <p class="text-white title-tag">CEO, ClinicGuideNG</p>
          <img src="../assets/linkedin.png" alt="">
        </div>

        <div class="container p-20">
          <img src="../assets/rect.png" alt="">
          <h3 class="text-white name-tag">
            Dr Adeola Olatunji
          </h3>
          <p class="text-white title-tag">CEO, ClinicGuideNG</p>
          <img src="../assets/linkedin.png" alt="">
        </div>
      </div>
    </div>
    <div class="bg-clinic-yellow">
      <div class="justify content-center">
          <p class="text-white text-center">
          © 2021 Copyright:
          <a
          href="#"
          class="text-white"
          >Clinic Guide NG. All rights reserved.</a
          >
          </p>
      
      </div>
  </div>
  </section>
</template>

<script>
// @ is an alias to /src
import Navbar from '@/components/Navbar.vue'

export default {
  components: {
    Navbar,
  }

}
</script>

<style scoped>
.text {
  font-size: 28px; 
  color: #002366;
}
.name-tag {
  font-size: 28px;
  font-weight: 900;
}
.title-tag {
  font-size: 28px;
  font-weight: 100;
}
.box{
  width: 362px;
  height: 462px;
  color: #002366;
}

.box-title{
  font-size: 49px;
  font-weight: 900;
}

</style>