<template>
  <div class=" hero-image   flex items-center justify-center border-y-4 w-full border-orange-300  relative p-10 text-center">
    <section class=" z-40 flex flex-col  items-center justify-center h-80 gap-2">
      <h2 class="text-2xl font-serif mb-8 text-white font-bold"> Visit us today and try our delicious pie and coffee</h2>
      <div class="flex gap-4 items-center justify-center ">
        <NuxtLink href="/contact">
          <v-btn size="x-large" color="orange-lighten-3">Contact</v-btn>
        </NuxtLink>
        <NuxtLink href="/">
          <v-btn size="x-large" variant="tonal" color="orange-lighten-3">Shop</v-btn>
        </NuxtLink>
      </div>
    </section>
    <div
      class="absolute z-40 -top-9 left-1/2 -translate-x-1/2 bg-black rounded-full p-1 shadow-md border-2 border-orange-300 hover:shadow-xl transition-all duration-150 ">
      <Icon name='ph:flower-lotus' class="text-amber-400 text-6xl" />
    </div>

    <div class="bg-black/40 absolute w-full h-full"></div>
  </div>
</template>

<script lang="ts" setup>

</script>

<style scoped>

.hero-image {
  height: 50vh;
  /* always scale the image to the appropriate size of your screen */
  background-size: cover;
  background-image: url('https://images.unsplash.com/photo-1525648199074-cee30ba79a4a?q=80&w=2070&auto=format&fit=crop&ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D');
  background-position: center;
  /* keeps the image fixed while scrolling , neat effect. */
  background-attachment: fixed;
  
}

</style>