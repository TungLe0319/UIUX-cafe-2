<script lang="ts" setup>
import './assets/css/tailwind.css'

</script>

<template>
  <div class="">
    <NuxtLayout>
   <v-app>

      
        <NuxtPage />
    
      </v-app>
    </NuxtLayout>
   
  </div>
</template>

<style>
.page-enter-active,
.page-leave-active {
  transition: all 0.20s;
}
.page-enter-from,
.page-leave-to {
  opacity: 0;
  filter: blur(0.5rem);
}
</style>