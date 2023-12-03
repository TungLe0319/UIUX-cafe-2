<template>
  <div class="p-20 w-full flex flex-col items-center justify-center space-y-3 ">
    <div class="text-center flex flex-col items-center justify-center space-y-4 ">
     <Icon name="line-md:coffee-twotone-loop"  class="text-orange-300 text-9xl"/>
      <div class="text-7xl   dancing-script ">
       Welcome to our  Café
      </div>
      <div class="w-full my-5">
        <IconDivider/>
      </div>
      <div class=" text-gray-500 ">
        Escape and unwind in a serene ambiance, where every moment is meant to be savored.
      </div>
    </div>

    
    <div class="w-2/3  shadow-xl   p-10">
    
   <div class="border-2 border-orange-200 p-5 py-20 flex flex-col items-center justify-center space-y-10 text-center">
       <a href="" class=" underline text-2xl">
          2540 E Fake Ave, Meridian, ID 84243
        </a>
        <a href="" class=" underline text-2xl">
          772-555-5555
        </a>
     <div class="">
         <p class="text-2xl">6AM - 3PM</p>
            <p class="text-2xl">5AM - 10PM</p>
            <p class="text-2xl">MONDAY - FRIDAY</p>


     </div>


          <div class="">
              <p class="text-2xl">8AM - 3PM</p>
            <p class="text-2xl">5AM - 10PM</p>
            <p class="text-2xl">SATURDAY & SUNDAY</p>
          </div>


          <div class="">Lorem ipsum dolor sit, amet consectetur adipisicing elit. Doloribus corporis laborum, in esse fugiat reprehenderit</div>

          <v-btn size="x-large" color="orange-lighten-3" class="text-white">
            Contact
          </v-btn>
   </div>
    </div>
  </div>
</template>

<script lang="ts" setup>
import IconDivider from './Globals/IconDivider.vue';


</script>

<style scoped></style>