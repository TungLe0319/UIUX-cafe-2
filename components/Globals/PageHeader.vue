<template>
  <div class="flex flex-col items-center  justify-center  mb-10 lg:mb-20">
    <div v-motion-pop-visible >
      <Icon name="pepicons-print:flower-bud" class="text-8xl text-orange-300 mb-10" />
    </div>
    <div v-motion-pop-visible class="text-5xl lg:text-7xl dancing-script">
      {{ title }}
    </div>
    <div v-motion-pop-visible class="w-full my-5">
      <IconDivider />
    </div>
    <div v-motion-pop-visible class="text-gray-500 my-8  text-center lg:px-40">
      {{ content }}
    </div>
  </div>
</template>

<script lang="ts" setup>
import IconDivider from './IconDivider.vue';




const expand = ref(false)
const props = defineProps(['title', 'content'])

</script>

<style></style>