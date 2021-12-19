<template>
  <nav class="bg-white shadow-lg">
    <div class="max-w-7xl md:mx-auto px-4">
      <div class="flex justify-between">
        <div class="flex space-x-7">
          <div>
            <!-- Website Logo -->
            <a href="/" class="flex items-center py-4 px-2">
              <img src="../assets/clinicguide.png" alt="Logo" class="mr-2" />
              <!-- <span class="font-semibold text-gray-500 text-lg">Navigation</span> -->
            </a>
          </div>
          <!-- Primary Navbar items -->
          <div class="hidden md:flex items-center justify-between space-x-2">
            <router-link
              to="/"
              class="py-4 px-2 border-blue-500 nav-navigation"
              active-class="border-b-4"
              >Home</router-link
            >
            <router-link
              to="/emergency"
              class="py-4 px-2 border-blue-500 hover:text-white-500 transition duration-300 nav-navigation"
              active-class="border-b-4"
              >Emergency Contacts</router-link
            >
            <router-link
              to="/blog"
              class="py-4 px-2 border-blue-500 hover:text-white-500 transition duration-300 nav-navigation"
              active-class="border-b-4"
              >Blog</router-link
            >
            <router-link
              to="/about"
              class="py-4 px-2 hover:text-white-500 border-blue-500 transition duration-300 nav-navigation"
              active-class="border-b-4"
              >About</router-link
            >
          </div>
        </div>
        <!-- Secondary Navbar items -->
        <div class="hidden md:flex items-center space-x-3">
          <router-link
            to="/review"
            class="p-2 font-bold text-white text-center bg-clinic-blue rounded-full transition duration-300"
            style="width: 160px; font-stretch: expanded;"
            >Leave A Review</router-link
          >
        </div>
        <!-- Mobile menu button -->
        <div class="md:hidden flex items-center">
          <button class="outline-none mobile-menu-button">
            <svg
              class="w-6 h-6 text-gray-500 hover:text-blue-500"
              x-show="!showMenu"
              fill="none"
              stroke-linecap="round"
              stroke-linejoin="round"
              stroke-width="2"
              viewBox="0 0 24 24"
              stroke="currentColor"
            >
              <path d="M4 6h16M4 12h16M4 18h16"></path>
            </svg>
          </button>
        </div>
      </div>
    </div>
    <!-- mobile menu -->
    <div class="hidden mobile-menu">
      <ul class="">
        <li class="active">
          <a
            href="/"
            class="block text-sm px-2 py-4 font-semibold mobile-nav transition duration-300"
            >Home</a
          >
        </li>
        <li>
          <a
            href="/emergency"
            class="block text-sm px-2 py-4 mobile-nav transition duration-300"
            >Emergency Contacts</a
          >
        </li>
        <li>
          <a
            href="/blog"
            class="block text-sm px-2 py-4 mobile-nav transition duration-300"
            >Blog</a
          >
        </li>
        <li>
          <a
            href="/about"
            class="block text-sm px-2 py-4 mobile-nav transition duration-300"
            >About</a
          >
        </li>
      </ul>
    </div>
  </nav>
</template>

<script>
export default {
  name: 'Navbar',
  // props: {
  //   msg: String
  // },
  mounted(){
    const btn = document.querySelector("button.mobile-menu-button");
      const menu = document.querySelector(".mobile-menu");

      btn.addEventListener("click", () => {
        menu.classList.toggle("hidden");
      });
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
h3 {
  margin: 40px 0 0;
}
ul {
  list-style-type: none;
  padding: 0;
}
li {
  display: inline-block;
  margin: 0 10px;
}

</style>
