<template>
  
  <Navbar />
  <body>
    <section class="justify-items-center max-w-7xl md:mx-auto px-4 h-full">
      <!-- <div class=""> -->
      <div class="grid lg:grid-cols-2 sm:relative md:grid-cols-none pb-10 lg:bg-none md:back-image">
        <div class="pt-10">
          <div class="flex landing-text">
            Find Healthcare <br> You Need, Anywhere You Are.
          </div>
          <p class="clinicblue" style="font-size: 24px">
            Find the best and most credible healthcare service providers near
            you.
          </p>
          <div class="p-3">
            <router-link to="/direction">
              <button
                class="
                  bg-transparent
                  font-bold
                  hover:text-white
                  py-2
                  px-4
                  landing-page-button1
                  hover:border-transparent
                  rounded-full
                "
                style="width: 223px"
              >
                Get Directions
              </button>
            </router-link>
            
            <router-link to="/review">
              <button
                class="
                  landing-page-button2
                  text-white
                  font-bold
                  py-2
                  px-4
                  rounded-full
                "
                style="width: 223px"
              >
                Leave a Review
              </button>
            </router-link>
            
          </div>
          <router-link to="/emergency">
            <button
              class="
                bg-transparent
                font-bold
                hover:text-white
                py-2
                px-4
                hover:border-transparent
                rounded-full
                landing-page-button3
                w-4/5
              "
            >
              Find Emergency Contacts
            </button>
          </router-link>
          
        </div>
        <div class="pt-10 hidden lg:inline-block">
          <img src="../assets/landing-image.svg" alt="landing-image" />
        </div>
      </div>
      <!-- </div> -->
    </section>
    <section class="max-w-7xl px-4">
      <div class="grid bg-blue justify-center lg:grid-cols-2 sm:grid-cols-1">
        <div class="lg:place-self-end mt-10">
          <div class="mapouter">
            <div class="gmap_canvas">
            <iframe
              width="100%"
              height="100%"
              id="gmap_canvas"
              src="https://maps.google.com/maps?q=%20Igbobi%20102216,%20Lagos&t=&z=13&ie=UTF8&iwloc=&output=embed"
              frameborder="0"
              scrolling="no"
              marginheight="0"
              marginwidth="0"
            ></iframe
            >
            
            </div>
          </div>
        </div>
        <div class="lg:content-start lg:ml-2 mt-10">
          
          <div class="address-card">
            <div class="">
              <h3 class="clinicblue text-center" style="font-weight: 900; font-size: 35px;">Top Picks For You:</h3>
              <hr class="mb-6 m-auto" style="width: 90%;">
              <div class="grid bg-blue grid-cols-4 ">
                <div class="text-center col-span-3 ">
                  <h4 class="hospital-name text-center">ClearEye Hospital</h4>
                  <p class="address-name text-center">41, Ago Palace Way, Lagos</p>
                </div>
                <div>
                  <img class="pl-10 pt-5 justify-self-end" src="../assets/arrow_right.png" alt="arrow">
                </div>
              </div>
              <hr class="my-6 m-auto" style="width: 90%;">
              <div class="grid bg-blue grid-cols-4 ">
                <div class="text-center col-span-3 ">
                  <h4 class="hospital-name">Way Maker Clinic</h4>
                  <p class="address-name">411, Akoka-Yaba, Lagos.</p>
                </div>
                <div>
                  <img class="pl-10 pt-5 justify-self-end" src="../assets/arrow_right.png" alt="arrow">
                </div>
              </div>
              <hr class="my-6 m-auto" style="width: 90%;">
              <div class="grid bg-blue grid-cols-4 ">
                <div class="text-center col-span-3 ">
                  <h4 class="hospital-name">Daystar Hospital</h4>
                  <p  class="address-name">57, Old Ojo Road, Lagos.</p>
                </div>
                <div>
                  <img class="pl-10 pt-5 justify-self-end" src="../assets/arrow_right.png" alt="arrow">
                </div>
              </div>
              <hr class="my-6 m-auto" style="width: 90%;">
              <div class="grid bg-blue grid-cols-4 ">
                <div class="text-center col-span-3 ">
                  <h4 class="hospital-name">Samaria Hospital</h4>
                  <p  class="address-name">04, Abule Oja Road, Lagos.</p>
                </div>
                <div>
                  <img class="pl-10 pt-5 justify-self-end" src="../assets/arrow_right.png" alt="arrow">
                </div>
              </div>
              <hr class="mt-4 w m-auto" style="width: 90%;">
              <p class="clinicblue text-center" style="font-weight: 900; font-size: 28px;">More Options</p>
            </div>
          </div>
          
        </div>
      </div>
    </section>
    <section class="justify-items-center md:hidden max-w-7xl md:mx-auto px-4 mt-10">
      <div class="bluecard">
        <div class="card-header shadow">
          <div class="grid h-full grid-cols-3 pt-5">
            <div class="card-header-text h-full text-center border-b-4 border-white-500">Add a center</div>
            <div class="card-header-text text-center">Contest a review</div>
            <div class="card-header-text text-center">Update Information</div>
          </div>
        </div>
        <div class="grid lg:grid-cols-5 lg:grid-rows-none md:grid-cols-none md:grid-rows-5 pt-10">
          <div class="lg:col-span-3 md:row-span-3 justify-center pl-10">
            <form class="justify-center">
              <div class="mb-4">
                <input class="card-input appearance-none border py-2 px-3 leading-tight focus:outline-none focus:shadow-outline" id="name" type="text" placeholder="Name">
              </div>
              <div class="mb-4 pt-10">
                <input class="card-input appearance-none border py-2 px-3 leading-tight focus:outline-none focus:shadow-outline" id="address" type="text" placeholder="Address">
              </div>
              <div class="mb-4 pt-10">
                <select class="card-input appearance-none border py-2 px-3 leading-tight focus:outline-none focus:shadow-outline" name="Category"  id="category" type="text" >
                  <option value="clinic">Clinic</option>
                  <option value="hospital">Hospital</option>
                  <option value="pharmacy">Pharmacy</option>
                </select>
              </div>
              
            </form>
            <p class="text-white font-bold">
              *addition may take up to a week for verification
            </p>
            
          </div>
          <div class="col-span-2 md:row-span-2 justify-center pr-10">
            <div class="frame content-center relative">
              <img class="absolute bottom-0 ml-10" src="../assets/user-plus.png" alt="">
              <div class="bg-white absolute bottom-0 place-self-center" style="height: 43px; width: 346px;">
                <div class="grid grid-cols-2 mt-2">
                  <img class="place-self-end pb-1" src="../assets/upload.png" alt="" style="">
                  <h3 class="text-left font-bold ml-2"> Upload</h3>
                </div>
                
              </div>
            </div>
            
            <div class="grid justify-center" style="width: 346px;">
              <button class="bg-clinic-yellow mt-5 text-white font-bold py-2 px-4 rounded-full focus:outline-none focus:shadow-outline" type="button" style="width:225px;">
                Leave A Review
              </button>
            </div>
            
          </div>
        </div>
        
        
      </div>
    </section>
    <section class="pt-10">
      <footer class="text-white">
        <div
        class="
          container
          justify-content-center
          px-5
          py-24
          mx-auto
          flex
          items-center
          md:flex-row md:flex-nowrap
          flex-wrap flex-col
        "
        >
          <div
            class="
            flex-grow flex flex-wrap
            mt-10
            md:text-center
            text-center
            "
          >
            <div class="lg:w-1/3 md:w-1/2 w-full px-4">
              <h2
                class="
                footer-header
                tracking-widest
                text-sm
                mb-3
                "
              >
                GET HELP
              </h2>
              <nav class="list-none mb-10">
                <li>
                <a href="" class="text-white hover:text-gray-800"
                  >Symptom Checker</a
                >
                </li>
                <li>
                <a href="" class="text-white hover:text-gray-800"
                  >Book A Consultation </a
                >
                </li>
                <li>
                <a href="" class="text-white hover:text-gray-800"
                  >Speak to a doctor</a
                >
                </li>
                
              </nav>
            </div>
            
            <div class="lg:w-1/3 md:w-1/2 w-full px-4">
            <h2
              class="
              footer-header
              tracking-widest
              text-sm
              mb-3
              "
            >
              READ NOW
            </h2>
            <nav class="list-none mb-10">
              <li>
              <a href="" class="text-white hover:text-gray-800"
                >Latest Issues</a
              >
              </li>
              <li>
              <a href="" class="text-white hover:text-gray-800"
                >Featured Issues</a
              >
              </li>
              <li>
              <a href="" class="text-white hover:text-gray-800"
                >Health Topics</a
              >
              </li>
            </nav>
            </div>
            <div class="lg:w-1/3 md:w-1/2 w-full px-4">
            <h2
              class="
              footer-header
              tracking-widest
              text-sm
              mb-3
              "
            >
              CLINICGUIDENG
            </h2>
            <nav class="list-none mb-10">
              <li>
              <a href="" class="text-white hover:text-gray-800"
                >Contact Us</a
              >
              </li>
              <li>
              <a href="" class="text-white hover:text-gray-800"
                >Privacy Policy</a
              >
              </li>
              <li>
              <a href="" class="text-white hover:text-gray-800"
                >FAQ</a
              >
              </li>
            </nav>
            </div>
          </div>
        </div>
        <div >
          <div
            class="justify content-center"
          >
            <p class="text-white-500 text-center">
            © 2021 Copyright:
            <a
              href="#"
              class="text-white"
              >Clinic Guide NG. All rights reserved.</a
            >
            </p>
            <!-- <span
            class="
              inline-flex
              sm:ml-auto sm:mt-0
              mt-2
              justify-center
              sm:justify-start
            "
            >
            <a href="" class="text-gray-500">
              <i class="fab fa-facebook-f"></i>
            </a>
            <a href="" class="ml-3 text-gray-500">
              <i class="fab fa-twitter"></i>
            </a>
            <a href="" class="ml-3 text-gray-500">
              <i class="fab fa-linkedin-in"></i>
            </a>
            <a href="" class="ml-3 text-gray-500">
              <i class="fab fa-youtube"></i>
            </a>
            <a href="" class="ml-3 text-gray-500">
              <i class="fab fa-instagram"></i>
            </a>
            </span> -->
          </div>
        </div>
      </footer>
    </section>
  </body>
</template>

<script>
// @ is an alias to /src
import Navbar from '@/components/Navbar.vue'

export default {
  name: 'Home',
  components: {
    Navbar
  }
}
</script>

<style scoped>
.back-image{
  background-image: url( ../assets/landing-mobile.png);
  image-rendering: auto;
}
  .bluecard {
    background-color: #002366;  
    width: 100%;
    max-width: 1196px;
    min-height: 630px;
    border-radius: 14px;
  }

  .address-card {
    background-color: #FF7F50;
    /* border-radius: 8px; */
    border-top-right-radius: 14px;
    border-bottom-right-radius: 14px;
    /* margin: auto; */
    width: 100%;
    max-width: 566px;
    min-width: auto;
    /* height: 630px; */
  }

  .card-header {
    height: 80px;
  }

  .card-header-text {
    color: white;
    font-size: 28px;
    font-weight: 400;
  }

  .card-input {
    width: 60%;
    max-width: 548px;
    height: 70px;
    background-color: #002366;
    font-weight: 700;
  }

  .mapouter {
    text-align: right;
    height: 630px;
    width: 100%;
  }
  
  .gmap_canvas {
    overflow: hidden;
    background: none !important;
    height: 630px;
    width: 100%;
  }

  .frame {
    border: 2px solid white;
    height: 100%; 
    width: 100%;
    max-height: 342px; 
    max-width: 346px;
  }
  .frame h3 {
    font-size: 21px;
    color: #002366;
  }
</style>