<script setup lang="ts">
import Button from './Globals/Button.vue'





</script>

<template>
  <main class="  relative ">
  
    <div class="flex w-full">
      <div class="w-1/2 card-img-background">
        <div class="px-2 py-10 rounded-md shadow-2xl bg-white text-black">
          <h3 class="text-6xl font-bold mb-2 text-center uppercase font-serif">Our Menu</h3>
          <p class=" p-10 text-center leading-loose"><strong>@Café Yun</strong>             customers can expect a culinary experience where every dish is meticulously crafted using top-quality ingredients, prepared to order. Our service strikes the perfect balance between personalized attention and a professional touch, all within vibrant and welcoming settings.</p>

          <div class="flex flex-col items-center justify-center space-y-4">
            <Button class="bg-emerald-400 shadow-xl hover:shadow-2xl transition-all !duration-300 uppercase">
             Order Online
            </Button>
              <Button class="bg-emerald-400 shadow-xl hover:shadow-2xl transition-all !duration-300 uppercase">
              View Menu
              </Button>
          </div>
        </div>
      </div>
      <div class="w-1/2">
        <img
          src="https://images.unsplash.com/photo-1592663527359-cf6642f54cff?q=80&w=1319&auto=format&fit=crop&ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D"
          alt="" class="">
      </div>
    </div>
    <div class="flex w-full">
      <div class="w-1/2">
        <img
          src="https://images.unsplash.com/photo-1583527825770-8bd0bfb1f1c1?q=80&w=1335&auto=format&fit=crop&ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D"
          alt="" class="">
      </div>
      <div class="w-1/2">
        <img
          src="https://images.unsplash.com/photo-1534432182912-63863115e106?q=80&w=1287&auto=format&fit=crop&ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D"
          alt="" class="">
      </div>
    </div>
    <div class="flex w-full">
      <div class="w-1/2">
        <img
          src="https://images.unsplash.com/photo-1609590981063-d495e2914ce4?q=80&w=1364&auto=format&fit=crop&ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D"
          alt="" class="">
      </div>
        <div class="w-1/2 card-img-background">
          <div class="px-2 py-10 rounded-md shadow-2xl bg-white text-black">
            <h3 class="text-6xl font-bold mb-2 text-center uppercase font-serif">We Cater</h3>
            <p class=" p-10 text-center leading-loose"><strong>Café Yun</strong> is delighted to extend an invitation to cater your upcoming event, whether it's a festive party, a crucial business meeting, or a corporate gathering. Our culinary expertise ensures a delightful experience for your guests. Discover the perfect blend of convenience and gourmet indulgence with Café Yun catering services—because every event deserves a touch of extraordinary taste.</p>

            <div class="flex flex-col items-center justify-center space-y-4">
              <Button class="bg-emerald-400 shadow-xl hover:shadow-2xl transition-all !duration-300 uppercase">
             Inquire Now
              </Button>
            
            </div>
          </div>
        </div>
    </div>
  </main>
</template>

<style scoped>
img {
  width: 100%;
  height: 100%;
  object-fit: cover;
}


.card-img-background {
  @apply bg-cover bg-center bg-no-repeat bg-fixed flex items-center justify-center p-20;

  background-image: url("https://images.unsplash.com/photo-1550537687-c91072c4792d?q=80&w=1287&auto=format&fit=crop&ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D");

  @media screen and (max-width: 768px) {

    @apply bg-scroll
  }
}
</style>
