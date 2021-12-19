<template>

  <Navbar/>
  <body>
    <section class="justify-items-center max-w-7xl md:mx-auto px-4">
      <div class="grid lg:grid-cols-4 md:grid-cols-1">
        <div class="lg:col-span-2 sm:relative mt-5">
          <img src="../assets/covid-image.png" alt="">
        </div>
        <div class="lg:pl-3 mt-5">
          <div class="relative">
            <h3 class="title inline">Featured</h3>
            <img class="inline absolute right-0 top-0" src="../assets/search-icon.png" alt="">
          </div>
          
          <div class="grid grid-rows-3">
            <div class="blog-card">
              <div class="grid relative lg:grid-cols-3 md:grid-cols-2">
                <div class="lg:col-span-2">
                  <h3 class="topic"> Nutrition</h3>
                  <h5 class="blog-title">Foods That Beat <br> Fatigue</h5>
                  <p class="blog-details">Adeola Olatunji / 10.08.2021</p>
                </div>
                <img class="inline absolute right-5 top-0" src="../assets/eggs.png" alt="">
              </div>
              <hr class="my-2">
            </div>
            <div class="blog-card mt-2">
              <div class="grid relative lg:grid-cols-3 md:grid-cols-2">
                <div class="lg:col-span-2">
                  <h3 class="topic"> Nutrition</h3>
                  <h5 class="blog-title">Foods That Beat <br> Fatigue</h5>
                  <p class="blog-details">Adeola Olatunji / 10.08.2021</p>
                </div>
                <img class="inline absolute right-5 top-0" src="../assets/eggs.png" alt="">
              </div>
              <hr class="my-2">
            </div>
            <div class="blog-card mt-2">
              <div class="grid relative lg:grid-cols-3 md:grid-cols-2">
                <div class="lg:col-span-2">
                  <h3 class="topic"> Nutrition</h3>
                  <h5 class="blog-title">Foods That Beat <br> Fatigue</h5>
                  <p class="blog-details">Adeola Olatunji / 10.08.2021</p>
                </div>
                <img class="inline absolute right-5 top-0" src="../assets/eggs.png" alt="">
              </div>
            </div>
          </div>
        </div>
      </div>
    </section>
    <section class="justify-items-center max-w-7xl md:mx-auto px-4 pt-10">
      <h3 class="title">Featured Health Topics</h3>
      <hr class="mb-3">
      <div class="grid lg:grid-cols-5 sm:col-span-1 justify-center">
        <div class="feature pt-3">
          <img src="../assets/covid.png" alt="">
          <h3 class="feature-text text-white font-bold">Covid-19</h3>
        </div>
        <div class="feature pt-3">
          <img src="../assets/wellness.png" alt="">
          <h3 class="feature-text text-white font-bold">Wellness</h3>
        </div>
        <div class="feature pt-3">
          <img src="../assets/nutrition.png" alt="">
          <h3 class="feature-text text-white font-bold">Nutrition</h3>
        </div>
        <div class="feature pt-3">
          <img src="../assets/longetivity.png" alt="">
          <h3 class="feature-text text-white font-bold">Longetivity</h3>
        </div>
        <div class="feature pt-3">
          <img src="../assets/sleep.png" alt="">
          <h3 class="feature-text text-white font-bold">Sleep</h3>
        </div>
      </div>
      <h3 class="title mt-2">Latest Stories</h3>
      <hr class="mb-3">
      <div class="grid lg:grid-cols-3 sm:grid-cols-1">
        <div class="story pt-3">
          <img src="../assets/healthy.png" alt="">
          <h3 class="topic">Nutrition</h3>
          <h5 class="blog-title">Eating Health With A Busy Schedule</h5>
          <p class="blog-details">Adeola Olatunji / 2 Hours Ago</p>
        </div>
        <div class="story pt-3">
          <img src="../assets/smiley.png" alt="">
          <h3 class="topic">Covid-19</h3>
          <h5 class="blog-title">Signs That You May Have Had Covid-19</h5>
          <p class="blog-details">Adeola Olatunji / 10 Hours Ago</p>
        </div>
        <div class="story pt-3">
          <img src="../assets/deep.png" alt="">
          <h3 class="topic">Sleep</h3>
          <h5 class="blog-title">What Is Deep Sleep And Why Is Important?</h5>
          <p class="blog-details">Adeola Olatunji / 16 Hours Ago</p>
        </div>
      </div>
    </section>
    <section class="justify-items-center max-w-7xl md:mx-auto px-4 pt-20">
      <h3 class="title">More Stories</h3>
      <hr class="mb-3">
      <div class="grid lg:grid-cols-2 sm:grid-cols-1">
        <div class="grid grid-cols-2 pt-3">
          <img src="../assets/guide.png" alt="">
          <div class="sm:m-2">
            <h3 class="topic">Nutrition</h3>
            <h5 class="blog-title">The Definitive Guide to Healthy Eating in Real Life</h5>
            <p class="blog-details">Adeola Olatunji / 12.05.2021</p>
          </div>
        </div>
        <div class="grid grid-cols-2 lg:ml-5 pt-3">
          <img src="../assets/bmi.png" alt="">
          <div>
            <h3 class="topic">Wellness</h3>
            <h5 class="blog-title">Is BMI an Accurate Predictor of Health?</h5>
            <p class="blog-details">Adeola Olatunji / 16.11.2020</p>
          </div>
        </div>
        <div class="grid grid-cols-2 pt-3">
          <img src="../assets/feet.png" alt="">
          <div>
            <h3 class="topic">Wellness</h3>
            <h5 class="blog-title">The 25 Best Diet Tips to Lose Weight and Improve Health</h5>
            <p class="blog-details">Adeola Olatunji / 17.02.2021</p>
          </div>
        </div>
        <div class="grid grid-cols-2 lg:ml-5 pt-3">
          <img src="../assets/woman.png" alt="">
          <div>
            <h3 class="topic">Women's Health</h3>
            <h5 class="blog-title">How to Exercise on Your Period</h5>
            <p class="blog-details">Adeola Olatunji / 14.03.2020</p>
          </div>
        </div>
        <div class="grid grid-cols-2">
          <img src="../assets/gold.png" alt="">
          <div>
            <h3 class="topic">Covid-19</h3>
            <h5 class="blog-title">Can Vitamin D Lower Your Risk of COVID-19?</h5>
            <p class="blog-details">Adeola Olatunji / 27.02.2020</p>
          </div>
        </div>
        <div class="grid grid-cols-2 ml-5">
          <img src="../assets/newbaby.png" alt="">
          <div>
            <h3 class="topic">Women's Health</h3>
            <h5 class="blog-title">Breastfeeding and Antibiotics: What You Need to Know</h5>
            <p class="blog-details">Adeola Olatunji / 10.08.2020</p>
          </div>
        </div>
      </div>
    </section>
    <section class="justify-items-center pt-10">
      <div class="bigger-card" style="min-height: 718px">
        <div class="container max-w-7xl md:mx-auto px-4 p-32">
          <h5 class="text-white text-center" style="font-weight:900px; font-size: 70px;">Stay Connected</h5>
          <p class="text-center text-white pt-10" style="font-size:28px;">Subscribe to our newsletter to stay connected to our activities, <br>
            get blogpost updates and sneakpeeks on what's happening in our community!</p>
          <div class="form pt-10 gap-4">
            <div>
              <input class="lg:inline sm:block p-2 lg:mr-5 mt-5 md:text-center" type="text" placeholder="Fullname">
              <input class="lg:inline sm:block p-2 lg:mr-5 mt-5 md:text-center" type="text" placeholder="Email Address">
              <button class="rounded-full text-white mt-5 px-5 py-1">Subscribe</button>
            </div>
          </div>
          <div class="grid lg:grid-cols-2 md:grid-cols-1 pt-10">
            <div class="contact">
              <h3 class="title text-center">Contact Us:</h3>
              <p class="text-center text-white" style="font-size:28px;">info@clinicguideng.com</p>
              <p class="text-center text-white" style="font-size:21px;">+234-812-345-6780</p>
            </div>
            <div class="socials place-self-center">
              <h3 class="title pt-5">Follow Us:</h3>
              <img class="inline p-3" src="../assets/f.png" alt="">
              <img class="inline p-3" src="../assets/linkedin.png" alt="">
              <img class="inline p-3" src="../assets/insta.png" alt="">
              <img class="inline p-3" src="../assets/twitter.png" alt="">
            </div>
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
  </body>
  
</template>

<script>
// @ is an alias to /src
import Navbar from '@/components/Navbar.vue';

export default {
  components: {
    Navbar,
  }

}
</script>

<style scoped>
::placeholder { /* Chrome, Firefox, Opera, Safari 10.1+ */
  color: white;
  opacity: 1; /* Firefox */
}

:-ms-input-placeholder { /* Internet Explorer 10-11 */
  color: white;
}

::-ms-input-placeholder { /* Microsoft Edge */
  color: white;
}

hr {
  border-color: #FF7F50;
} 

.title {
  color: #002366;
  font-size: 35px;
  font-weight: 900;
}

.blog-card {
  width: 466px;
  height: 160px;
}

.topic {
  font-size: 28px;
  color: #FF7F50;
}

.blog-title {
  font-size: 28px;
  color: #002366;
  font-weight: 900;
}

.blog-details {
  font-size: 21px;
  color: #002366;
}

.feature {
  position: relative;
  text-align: center;
}

.feature-text {
  position: absolute;
  font-size: 28px;
  top: 50%;
  left: 50%;
  transform: translate(-50%, -50%);
}
.form {
  display: grid;
  place-items: center;
}

.form input {
  border-bottom: 2px solid gray;
  background-color: #FF7F50;
  width: 345px;
  font-size: 24px;
}

.form button {
  background-color: #002366;
  font-size: 24px;
}

.contact .title {
  color: white;
}

.contact p {
  color: white;
  font-size: 28px;
}

.socials .title {
  color: white;

}
</style>