<template>
  <div class="grid  md:grid-cols-2 lg:grid-cols-4 gap-4 p-10 bg-zinc-900">
    <div v-for="item in items" class="  group transition-all duration-200 hover:scale-[1.02] relative">
      <Button class="w-full !p-0">
        <img :src="item.src" alt="coffee cup icon" class=" shadow-2xl w-full h-full object-cover">
        <div
          class="absolute  inset-0 w-full h-full flex items-center justify-center opacity-0 hover:opacity-100 transition-all duration-300 border-8 border-white/40  bg-black/40 scale-0 group-hover:scale-100   ease-in-out ">
          <div class="p-2 bg-black/60 border-4  w-full h-full flex items-center justify-center  scale-90 ">
            <h2 class="text-white text-3xl font-bold ">
              {{ item.title }}
            </h2>
          </div>
        </div>
      </Button>
    </div>
  </div>
</template>

<script lang="ts" setup>
import Button from './Globals/Button.vue';
const items = [
  {
    src: 'https://images.unsplash.com/photo-1517701550927-30cf4ba1dba5?q=80&w=1287&auto=format&fit=crop&ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D',
    title: 'Iced Coffee'
  },
  {
    src: 'https://images.unsplash.com/photo-1530373239216-42518e6b4063?q=80&w=1287&auto=format&fit=crop&ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D'
    , title: 'Caramel Mocha Oreo Frappe'
  },
  {
    src: 'https://images.unsplash.com/photo-1549652127-2e5e59e86a7a?q=80&w=1287&auto=format&fit=crop&ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D'
    , title: 'Cold Brew'
  }
  ,
  { src: 'https://images.unsplash.com/photo-1562878424-0da674456d33?q=80&w=1287&auto=format&fit=crop&ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D', title: 'Cold Brew Plain' }
  ,
  { src: 'https://images.unsplash.com/photo-1561817245-de553dfe2e88?q=80&w=1288&auto=format&fit=crop&ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D', title: 'Vegan Chocolate Cupcakes' }
  ,
  {
    src: 'https://images.unsplash.com/photo-1586657263857-346c4b712ff5?q=80&w=1364&auto=format&fit=crop&ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D'
    , title: 'Croissants'
  }
  ,
  { src: 'https://images.unsplash.com/photo-1627308595260-6fad84c40413?q=80&w=1335&auto=format&fit=crop&ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D', title: 'Bagels' }
  ,
  { src: 'https://images.unsplash.com/photo-1645621479479-4ebaa3dbf801?q=80&w=1227&auto=format&fit=crop&ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D', title: 'Avocado Toast' }
  ,

]
</script>

<style scoped>
img {
  width: 100%;
  height: 30rem;
  object-fit: cover;



  @media screen and (max-width: 762px) {
    height: 15rem;
  }

  @media screen and (max-width: 1024px) {
    height: 25rem;

  }

  @media screen and (max-width: 1280px) {
    height: 30rem;

  }

  @media screen and (max-width: 1536px) {
    height: 35rem;
  }

  @media screen and (max-width: 1920px) {
    height: 40rem;

  }
}


/* Add this to your existing stylesheet */
</style>