<script lang="ts" setup>
import CallToAction from '~/components/Globals/CallToAction.vue';

import BusinessHours from '~/components/Index/BusinessHours.vue';
import Hero from '~/components/Index/Hero.vue';
import LandingPhotoGallery from '~/components/Index/LandingPhotoGallery.vue';
import Testimonials from '~/components/Index/Testimonials.vue';
</script>

<template>
  <div class="flex flex-col  ">
    <Hero />
    <BusinessHours />
    <LandingPhotoGallery />
    <Testimonials />
    <CallToAction />
  </div>
</template>


<style scoped></style>
