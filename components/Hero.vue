<script lang="ts" setup>


</script>

<template>
  
 <v-carousel height="100vh" draggable="true" progress="true">
    <v-carousel-item draggable="true"
      src="https://images.unsplash.com/photo-1543339308-43e59d6b73a6?q=80&w=2070&auto=format&fit=crop&ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D"
      cover
    ></v-carousel-item>

    <v-carousel-item draggable="true"
      src="https://images.unsplash.com/photo-1511994714008-b6d68a8b32a2?q=80&w=2070&auto=format&fit=crop&ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D"
      cover
    ></v-carousel-item>

    <v-carousel-item draggable="true"
      src="https://images.unsplash.com/photo-1625944525533-473f1a3d54e7?q=80&w=1928&auto=format&fit=crop&ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D"
      cover
    ></v-carousel-item>
  </v-carousel>
  <v-divider></v-divider>
</template>

<style scoped>
img{
  @apply hover:brightness-100
}
</style>
