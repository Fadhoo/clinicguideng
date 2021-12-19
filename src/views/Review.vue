<template>
  <Navbar/>
  <section class="justify-center max-w-7xl md:mx-auto px-4">
      <div class="grid grid-cols-3 pt-10 " style="width: 1080px">
        <div class="border-line h-20 col-span-1 grid grid-cols-3">
          <div class="filter">
            <h3>Hospital</h3>
          </div>
          <div class="filter">
            <h3>Clinic</h3>
          </div>
          <div class="filter pr-5">
            <h3>Pharmacy</h3>
          </div>
        </div>

        <div class="col-span-2 relative">
          <input class="border-line pl-4 w-full focus:outline-none text-2xl"
            type="search" name="search" placeholder="Search Here">
          <button type="submit" class="absolute right-0 top-0 mt-3 mr-4">
            <img src="../assets/search-icon.png" alt="">
          </button>
        </div>
          


      </div>
      <div class="card bg-clinicyellow mt-10" style="width: 1196px; height: 310px; border-radius: 14px;">
        <div class="grid grid-cols-4">
          <div class="place-self-start bluecard">
            <div class="card-body content-center pl-10 pt-5">
              <h5 class="card-title" style="font-size: 21px;">
                Customer Reviews
              </h5>
              <div class="pill mt-3 justify-center rounded-full px-5">
                <img class="inline " src="../assets/star.png" alt="star">
                <img class="inline " src="../assets/star.png" alt="star">
                <img class="inline " src="../assets/star.png" alt="star">
                <img class="inline " src="../assets/star.png" alt="star">
                <img class="inline" src="../assets/star.png" alt="star">

                <p class="pl-1 inline text place-self-end">4.7 out of 5</p>
              </div>

              <p class="pl-10 text-white" style="font-size: 11px;">37 customer ratings</p>
              <div class="grid grid-cols-7 pt-5">
                <p class="text inline" style="white-space: nowrap;">5 star</p>
                <div class="progress-bar bg-white col-span-5 rounded-full"> 
                  <div class="progress-bar rounded-full block bg-clinic-yellow" style="height: 100%; width:84%; border-color: #FF7F50; border-width: 3px;"></div>
                </div>
                <p class="text mr-10">84%</p>
              </div>
              <div class="grid grid-cols-7 pt-3">
                <p class="text inline" style="white-space: nowrap;">4 star</p>
                <div class="progress-bar bg-white col-span-5 rounded-full"> 
                  <div class="progress-bar rounded-full block bg-clinic-yellow" style="height: 100%; width:9%; border-color: #FF7F50; border-width: 3px;"></div>
                </div>
                <p class="text mr-10">9%</p>
              </div>
              <div class="grid grid-cols-7 pt-3">
                <p class="text inline" style="white-space: nowrap;">3 star</p>
                <div class="progress-bar bg-white col-span-5 rounded-full"> 
                  <div class="progress-bar rounded-full block bg-clinic-yellow" style="height: 100%; width:4%; border-color: #FF7F50; border-width: 3px;"></div>
                </div>
                <p class="text mr-10">4%</p>
              </div>
              <div class="grid grid-cols-7 pt-3">
                <p class="text inline" style="white-space: nowrap;">2 star</p>
                <div class="progress-bar bg-white col-span-5 rounded-full"> 
                  <div class="progress-bar rounded-full block bg-clinic-yellow" style="height: 100%; width:2%; border-color: #FF7F50; border-width: 3px;"></div>
                </div>
                <p class="text mr-10">2%</p>
              </div>
              <div class="grid grid-cols-7 pt-3">
                <p class="text inline" style="white-space: nowrap;">1 star</p>
                <div class="progress-bar bg-white col-span-5 rounded-full"> 
                  <div class="progress-bar rounded-full block bg-clinic-yellow" style="height: 100%; width:1%; border-color: #FF7F50; border-width: 3px;"></div>
                </div>
                <p class="text mr-10">1%</p>
              </div>
            </div>
          </div>
          <div class="card-body pl-10 col-span-3">
            <h3 class="card-title inline mt-5">
              ClearEye Hospital <p class="inline body-text"> (1.3 miles away)</p>
            </h3>
            <hr class="mb-4" style="width: 821px;">

            <p class="card-text">“The nurses were very accomodating and friendly. Enjoyed their service and ambience.”</p>
            <p class="text-right mr-20 body-text">Ayotunde</p>

            <hr class="my-4" style="width: 821px;">

            <p class="card-text">“The doctor was friendly, but the nurses kept making mistakes and messing up.”</p>
            <p class="text-right mr-20 body-text">Debbie</p>

            <hr class="my-4" style="width: 821px;">

            <h4 class="text-center card-text">More Reviews</h4>

          </div>
        </div>
        

      </div>
  </section>
  <section class="justify-center max-w-7xl md:mx-auto px-4 pt-20">
    <div class="experience lg:ml-20"><h3>Tell Us Your Experience</h3></div>

    <div class="grid justify-center grid-rows-3 ml-10">
      <div class="p-3">
        <div class="place-self-start inline">
          <img class="inline p-3" src="../assets/big-star.png" alt="">
          <img class="inline p-3" src="../assets/big-star.png" alt="">
          <img class="inline p-3" src="../assets/big-star.png" alt="">
          <img class="inline p-3" src="../assets/big-star.png" alt="">
          <img class="inline p-3" src="../assets/big-star.png" alt="">
        </div>
        <div class="inline ml-20">
          <input class="bg-white pl-5" type="text" placeholder="Name*" style="color: #002366; width: 362px; height: 70px; font-size:28px; border-color: #002366; border-width: 3px; border-radius: 14px;">
        </div>
      </div>
      <div class="row-span-2 mt-5">
        
        <input class="bg-white pl-5" type="text" placeholder="Review*" style="color: #002366; width: 979px; height: 196px; font-size:28px; border-color: #002366; border-width: 3px; border-radius: 14px;">

      </div>
      <div class="grid justify-center">
        <button class="bg-clinic-blue mt-5 text-white font-bold py-2 px-4 rounded-full focus:outline-none focus:shadow-outline" type="button" style="width:225px;">
          Leave A Review
        </button>
      </div>
    </div>
  </section>
  <section class="justify-center max-w-7xl md:mx-auto px-4 pt-20">
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
</template>

<script>
import Navbar from '@/components/Navbar.vue';


export default {
  name: 'Review',
  components: {
    Navbar
  }
}
</script>

<style>
.search-bar {
    height: 1080px;
    width: 70px;
}

.filter {
  place-self: center;
  color: #002366;
  font-size: 21px;
  font-weight: 700;
}

.filter-option {
  border: black;
}

.progress-bar {
  border-style: solid;
  border-width: 2px;
  width: 155px;
  height: 11px;
  position: relative;
}

.text {
  color: white;
  font-size: 11px;
}

.border-line {
  border-style: solid;
  height: 70px;
  background-color: white;
  border-width: 2px;
  border-radius: 5px;
}

.bluecard {
  background-color: #002366;  
  width: 310px;
  height: 310px;
  border-radius: 14px;
}

.pill{
  background-color: white;
  height: 22px;
  width: 199px;  
}

.pill .text {
  color: #002366;
  font-weight: 700;
}

.card-title {
  font-size: 32px;
  color: white;
  font-weight: 700;
}

.card-body {
  padding: auto;
}

.body-text {
  font-size: 21px;
  color: white;
}

.card-text {
  font-size: 21px;
  color: white;
  font-weight: 700;
  text-shadow: 2px 2px rgb(87, 87, 87);

}
.experience {
  color: #002366;
  font-size: 56px;
  font-weight: 900;
}
</style>