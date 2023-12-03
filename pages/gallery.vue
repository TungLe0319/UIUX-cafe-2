<template>
  <main class="flex flex-col items-center justify-center  bg-amber-800/30 ">
    <v-sheet color=" p-4 lg:p-20 ">
      <div class="w-full flex items-center justify-center">
        <div class=" lg:w-2/3   text-center  my-20">
          <h1 class=" text-2xl lg:text-4xl ">
            Lorem ipsum dolor, sit amet consectetur adipisicing elit. Doloribus accusamus voluptates.
          </h1>
          <IconDivider class="my-5" />
        </div>
      </div>
      <div class="w-full">
        <v-row>
          <template v-for="(image, imgIdx) in imageLayout" :key="imgIdx">
            <v-col :cols="image.cols">
              <v-img :src="`https://picsum.photos/1500/750?image=${image.cols * 20}`" cover height="100%"
                class=" shadow-xl"></v-img>
            </v-col>
            <v-col v-if="image.children" cols="6" class="d-flex flex-column">
              <v-row>
                <v-col v-for="(children, childIdx) in image.children" :key="childIdx" :cols="children.cols">
                  <v-img :src="`https://picsum.photos/1500/1000?image=${children.cols + childIdx}`" cover height="100%"
                    class="shadow-xl hover:scale-[1.02] transition-all duration-200 "></v-img>
                  
                </v-col>
              </v-row>
            </v-col>
          </template>
        </v-row>
      </div>
      <div class="flex flex-col items-center justify-center">
        <div class="w-full flex items-center justify-center">
          <div class=" lg:w-2/3   text-center  my-20">
            <h1 class=" text-2xl lg:text-4xl ">
              Lorem ipsum dolor, sit amet consectetur adipisicing elit. Doloribus accusamus voluptates.
            </h1>
            <IconDivider class="my-5" />
          </div>
        </div>
        <div class="flex gap-2  ">
          <img src="https://themes.muffingroup.com/be/cafe2/wp-content/uploads/2017/09/home_cafe2_gallery5.jpg" alt=""
            class="w-1/2">
          <img src="https://themes.muffingroup.com/be/cafe2/wp-content/uploads/2017/09/home_cafe2_gallery6.jpg" alt=""
            class="w-1/2">
        </div>
      </div>
    </v-sheet>
    <CallToAction title="Visit us today and try our delicious pie and coffee" />
  </main>
</template>

<script lang="ts" setup>
import IconDivider from '~/components/Globals/IconDivider.vue';

const imageLayout = [
  { cols: 4 },
  {
    cols: 8,
    children: [{ cols: 12 }, { cols: 12 }],
  },
  { cols: 6 },
  { cols: 3 },
  { cols: 9 },
  { cols: 4 },
  { cols: 8 },
]
</script>

<style scoped>
img {
  @apply shadow-2xl
}



</style>