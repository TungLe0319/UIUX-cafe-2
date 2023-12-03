<template>
   <div class="flex flex-col items-center justify-center w-full lg:px-40">
        <div class=" text-center w-2/3 my-8">
          <h1 class="text-7xl  dancing-script  ">Our Photo Gallery</h1>
           <div class="w-full my-5">
          <IconDivider/>
        </div>
          <div class="my-8 text-gray-500  text-center "> Lorem ipsum, dolor sit amet consectetur adipisicing elit. Cum aliquam, nesciunt quia temporibus sunt magni,
            quod obcaecati eligendi similique repellendus vero voluptas recusandae eius, veniam at est nemo quidem ad.</div>
        </div>
      </div>
      <div class="flex flex-col items-center justify-center space-y-4">
        <Icon name="mingcute:leaf-3-fill"  />
        <div class="flex items-center justify-center space-x-4 p-10 relative">
          <Icon name="fluent:leaf-three-16-filled"  />
          <div class="   w-3/4">
            <img
              src="https://images.unsplash.com/photo-1559925393-8be0ec4767c8?q=80&w=1471&auto=format&fit=crop&ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D"
              alt="" class="  ">
          </div>
          <Icon name="fluent:leaf-three-16-filled"  />
          <div class="absolute bottom-4">
            <NuxtLink
             to="/gallery">
            <div class="lg:hidden">
              
                  <v-btn   color="orange-lighten-3" elevation="5" class="text-white" >View All Photos</v-btn>
             
            </div>
            <div class="hidden lg:block">
                   <v-btn size="x-large" color="orange-lighten-3" elevation="5" class="text-white" >View All Photos</v-btn>
                
            </div>
            </NuxtLink>
          </div>
        </div>
       <div class=" lg:pt-5">
         <Icon name="mingcute:leaf-3-fill"  />
       </div>
      </div>
</template>

<script lang="ts" setup>
import IconDivider from '../Globals/IconDivider.vue';


</script>

<style scoped>
.icon {
  @apply text-6xl text-amber-400 drop-shadow-md hover:rotate-180 transition-all duration-300
}
</style>