<script lang="ts" setup>
import Hero from '../components/Hero.vue'
</script>

<template>
  <div class="flex flex-col  ">
    <Hero />
    <BusinessHours />
  <LandingPhotoGallery/>
  <Testimonials/>
  </div>
</template>


<style scoped>
.icon {
  @apply text-6xl text-amber-400 drop-shadow-md hover:rotate-180 transition-all duration-300
}
</style>
