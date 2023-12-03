<template>
  <div class=" bg-white border-y-2 w-full border-gray-400 relative p-10 text-center">
    <div class=" flex flex-col  items-center justify-center h-80 gap-2">
      <h2 class="text-2xl font-serif mb-8"> {{ title
      }}</h2>
      <div class="flex gap-4 items-center justify-center ">
        <NuxtLink href="/contact">
          <v-btn size="x-large" color="orange-lighten-3">Contact</v-btn>
        </NuxtLink>
        <NuxtLink href="/shop">
          <v-btn size="x-large" variant="outlined" color="orange-lighten-3">Shop</v-btn>
        </NuxtLink>
      </div>
    </div>
    <div
      class="absolute -top-8 left-1/2 -translate-x-1/2 bg-black rounded-full p-1 shadow-md border-2 border-orange-300 hover:shadow-xl transition-all duration-150 ">
      <Icon name='ph:flower-lotus' class="text-amber-400 text-6xl" />
    </div>
  </div>
</template>

<script lang="ts" setup>
const props = defineProps({
  title: {
    type: String,
    required: true
  }
})
</script>

<style scoped></style>