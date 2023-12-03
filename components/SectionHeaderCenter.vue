<script lang="ts" setup>
import IconDivider from './Globals/IconDivider.vue';

defineProps(['header', 'title', 'content'])
</script>

<template>
  <div class="mb-4 flex flex-col items-center justify-center space-y-6">
    <h3 class=" uppercase text-orange-400">
      {{ header }}
    </h3>
    <h1 class=" text-2xl font-bold lg:text-4xl  text-center ">
      {{ title }}
    </h1>
    <div class="w-full">
      <IconDivider/>
    </div>
    <div class="w-3/4 px-10 font-medium  text-center lg:w-1/2 lg:px-0 lg:text-center">
      <p>{{ content }}</p>
    </div>
  </div>
</template>

<style>
/* Add your styles here */
</style>
