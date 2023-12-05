
<script setup>

import IconDivider from "./Globals/IconDivider.vue";
const scrollToTop = () => {
  window.scrollTo({ top: 0, behavior: 'smooth' });
};
</script>
<template>
  <div class="w-full my-40 flex items-center justify-center  text-black">
    <div class="md:w-2/3 w-full px-4  flex flex-col">
      <div class="w-full text-7xl font-bold font-serif">
        <h1 v-motion-slide-visible-once-top class="w-full md:w-2/3">We give you our thanks.</h1>
      </div>
      <div class="flex mt-8 flex-col md:flex-row md:justify-between">
        <p v-motion-slide-visible-once-top class="w-full md:w-2/3 text-gray-500">Fostering success through dedicated
          service. Navigate questions with our
          committed assistance, ensuring your experience is met with tailored solutions. </p>
        <div v-motion-slide-visible-once-right class=" pt-6 md:pt-0 space-x-4">
          <NuxtLink to="/contact">
            <v-btn size="x-large" color="orange-lighten-3">Contact</v-btn>
          </NuxtLink>
          <v-btn @click="scrollToTop" class="orange-lighten-3" icon=" mdi-arrow-up" size="large"></v-btn>
        </div>
      </div>
      <div class="flex flex-col">
        <div v-motion-slide-visible-left :delay="200" class="flex mt-24 mb-12 flex-row justify-between text-center items-center">
          <a 
            class=" hidden md:block cursor-pointer text-gray-600 hover:text-white uppercase">About</a>
          <a 
            class="hidden md:block cursor-pointer text-gray-600 hover:text-white uppercase">Services</a>
          <a 
            class="hidden md:block cursor-pointer text-gray-600 hover:text-white uppercase">Why us</a>
          <a 
            class="hidden md:block cursor-pointer text-gray-600 hover:text-white uppercase">Contact</a>
          <div v-motion-slide-visible-right :delay="200" class="flex flex-row space-x-8 items-center justify-between">
            <a href="/">
              <Icon name="uil:facebook" class="text-4xl" />
            </a>
            <a href="/">
              <Icon name="uil:instagram" class="text-4xl" />
            </a>
            <a href="/">
              <Icon name="uil:youtube" class="text-4xl" />
            </a>
            <a href="/">
              <Icon name="fa6-brands:x-twitter" class="text-4xl" />
            </a>
          </div>
        </div>
        <IconDivider />
        <p class="w-full text-center my-12 text-gray-600">Copyright © 2023 Lorem Co.</p>
      </div>
    </div>
  </div>
</template>


<style lang="css" scoped>
a {
  @apply hover:-translate-y-1 transition-all duration-200
}</style>