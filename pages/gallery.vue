<template>
  <main class="  ">
     <PageHeader title="What we do" content="  Lorem ipsum dolor sit amet, consectetur adipisicing elit. Consequuntur, corporis similique. Maxime corrupti possimus
      exercitationem."/>
    <v-sheet color=" p-4 lg:px-20 ">
     
      <section class="w-full  my-20 lg:my-40">
        <v-row>
          <template v-for="(image, imgIdx) in imageLayout" :key="imgIdx">
            <v-col :cols="image.cols">
              <v-img :src="`https://picsum.photos/1500/750?image=${image.cols * 20}`" cover height="100%"
                class=" shadow-xl hover:scale-[1.02] transition-all duration-200"></v-img>
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
      </section>
     <section>
     
        <Coffee />
     </section>
      <section class="flex flex-col items-center justify-center mb-20 lg:mb-0">
           <div class="flex flex-col items-center  justify-center  my-10  ">
          <div class="text-4xl  ">Lorem Ipsum Dolur</div>
          <div class="w-full my-5">
            <IconDivider />
          </div>
          <div class=" text-center text-gray-500 my-8 w-2/3">Lorem ipsum dolor sit amet consectetur adipisicing elit. Nam
            accusantium quibusdam quos! Velit, incidunt eius!</div>
        </div>
        <div class="flex flex-col lg:flex-row gap-5  my-10  ">
          <img src="https://themes.muffingroup.com/be/cafe2/wp-content/uploads/2017/09/home_cafe2_gallery5.jpg" alt=""
            class="lg:w-1/2  ">
          <img src="https://themes.muffingroup.com/be/cafe2/wp-content/uploads/2017/09/home_cafe2_gallery6.jpg" alt=""
            class="lg:w-1/2">
        </div>
      </section>
    </v-sheet>
    <CallToAction  />
  </main>
</template>

<script lang="ts" setup>
import Coffee from '~/components/Gallery/Coffee.vue';
import CallToAction from '~/components/Globals/CallToAction.vue';
import IconDivider from '~/components/Globals/IconDivider.vue';
import PageHeader from '~/components/Globals/PageHeader.vue';


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