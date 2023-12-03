<template>
  <main class=" ">
    <PageHeader title="Our Story" content="  Lorem ipsum dolor sit amet, consectetur adipisicing elit. Consequuntur, corporis similique. Maxime corrupti possimus
      exercitationem."/>
    <v-sheet class="lg:p-20">
  
      <v-carousel>
        <v-carousel-item src="https://themes.muffingroup.com/be/cafe2/wp-content/uploads/2017/09/home_cafe2_ourcafe3.jpg"
          cover></v-carousel-item>
        <v-carousel-item src="https://themes.muffingroup.com/be/cafe2/wp-content/uploads/2017/09/home_cafe2_ourcafe3.jpg"
          cover></v-carousel-item>
        <v-carousel-item src="https://themes.muffingroup.com/be/cafe2/wp-content/uploads/2017/09/home_cafe2_ourcafe2.jpg"
          cover></v-carousel-item>
      </v-carousel>
    
      <section v-for="section in sections" class="lg:flex   my-10 lg:my-20">
        <div class="  lg:w-1/2  flex flex-col items-center justify-center  ">
         <span class="text-4xl  font-serif mb-5">
           {{ section.title }}
         </span>
       
          <img :src="section.image" alt="image of a restaurant" class=" w-2/3">
       
        </div>
        <div class=" lg:w-1/2 p-10  leading-8">
          <strong class="text-8xl  dancing-script text-orange-300">{{ section.content.charAt(0) }} </strong>
          {{ section.content }}
        </div>
      </section>
   
      <div class="flex flex-col items-center  justify-center  my-10 lg:my-20">
      
        <div class="text-4xl font-serif text-center"> Lorem ipsum dolor sit. </div>
        <div class="w-full pt-8">
          <IconDivider />
        </div>
        <div class="w-2/3 text-center my-8 text-gray-500">
          <p>Lorem, ipsum dolor sit amet consectetur adipisicing elit. Amet, iure optio rem nihil placeat laboriosam id
            tempora aliquid quam, maxime eligendi dolorem eum quisquam eius!</p>
        </div>
        <div class=" flex flex-col space-y-5 items-center justify-center ">
          <NuxtLink to="/contact">
            <v-btn size="x-large" color="orange-lighten-3">Contact</v-btn>
          </NuxtLink>
          <NuxtLink to="/">
            <v-btn size="x-large" variant="outlined" color="orange-lighten-3">Shop</v-btn>
          </NuxtLink>
        </div>
      </div>
    </v-sheet>
   <CallToAction/>
  </main>
</template>

<script lang="ts" setup>
import CallToAction from '~/components/Globals/CallToAction.vue';
import IconDivider from '~/components/Globals/IconDivider.vue';
import PageHeader from '~/components/Globals/PageHeader.vue';

const sections = [
  {
    title: 'Where we started',
    image:'https://images.unsplash.com/photo-1614932459212-d3bd65a6660a?q=80&w=1970&auto=format&fit=crop&ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D',
    content: 'Lorem ipsum dolor sit amet consectetur adipisicing elit. Fugit ea fuga ducimus pariatur ullam. Earum iste laboriosam fugit sapiente et aspernatur perspiciatis assumenda adipisci enim, molestias voluptas officia modi sint maiores hic tenetur optio harum, consectetur sunt quae quaerat. Tempora inventore modi excepturi molestiae enim, consectetur numquam odit perspiciatis velit architecto dignissimos voluptate quo corporis tenetur ad distinctio aliquam atque saepe quia doloribus vitae ea dolores at? Esse iure nemo sunt incidunt adipisci quaerat sapiente, voluptatum eveniet quisquam vitae magnam vel rerum autem? Doloremque facere nam ut ab dolor ea quisquam iste libero perferendis in, impedit sit amet fugiat optio aut. Perspiciatis cupiditate culpa, minus voluptatum, dolorum non a molestiae sed iure quae sunt inventore earum ducimus porro quis quasi nihil totam eligendi quisquam. Quasi illo, adipisci iste numquam debitis excepturi ipsum explicabo magni voluptatum ab labore odio autem vitae in earum quisquam, iure maiores ex quos qui aperiam nihil enim eum! Quis excepturi iusto optio pariatur quibusdam non, vero illum minima sunt fugit consequatur harum perferendis incidunt ipsa tenetur labore.quisquam.'
  },
  {
    title: 'Where we are',
    image:'https://images.unsplash.com/photo-1569096651661-820d0de8b4ab?q=80&w=1926&auto=format&fit=crop&ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D',
    content: 'It amet consectetur adipisicing elit. Fugit ea fuga ducimus pariatur ullam. Earum iste laboriosam fugit sapiente et aspernatur perspiciatis assumenda adipisci enim, molestias voluptas officia modi sint maiores hic tenetur optio harum, consectetur sunt quae quaerat. Tempora inventore modi excepturi molestiae enim, consectetur numquam odit perspiciatis velit architecto dignissimos voluptate quo corporis tenetur ad distinctio aliquam atque saepe quia doloribus vitae ea dolores at? Esse iure nemo sunt incidunt adipisci quaerat sapiente, voluptatum eveniet quisquam vitae magnam vel rerum autem? Doloremque facere nam ut ab dolor ea quisquam iste libero perferendis in, impedit sit amet fugiat optio aut. Perspiciatis cupiditate culpa, minus voluptatum, dolorum non a molestiae sed iure quae sunt inventore earum ducimus porro quis quasi nihil totam eligendi quisquam. Quasi illo, adipisci iste numquam debitis excepturi ipsum explicabo magni voluptatum ab labore odio autem vitae in earum quisquam, iure maiores ex quos qui aperiam nihil enim eum! Quis excepturi iusto optio pariatur quibusdam non, vero illum minima sunt fugit consequatur harum perferendis incidunt ipsa tenetur labore.quisquam.'
  },
  {
    title: 'Where we are going',
    image:'https://images.unsplash.com/photo-1467003909585-2f8a72700288?q=80&w=1974&auto=format&fit=crop&ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D',
    content: 'Consectetur adipisicing elit. Fugit ea fuga ducimus pariatur ullam. Earum iste laboriosam fugit sapiente et aspernatur perspiciatis assumenda adipisci enim, molestias voluptas officia modi sint maiores hic tenetur optio harum, consectetur sunt quae quaerat. Tempora inventore modi excepturi molestiae enim, consectetur numquam odit perspiciatis velit architecto dignissimos voluptate quo corporis tenetur ad distinctio aliquam atque saepe quia doloribus vitae ea dolores at? Esse iure nemo sunt incidunt adipisci quaerat sapiente, voluptatum eveniet quisquam vitae magnam vel rerum autem? Doloremque facere nam ut ab dolor ea quisquam iste libero perferendis in, impedit sit amet fugiat optio aut. Perspiciatis cupiditate culpa, minus voluptatum, dolorum non a molestiae sed iure quae sunt inventore earum ducimus porro quis quasi nihil totam eligendi quisquam. Quasi illo, adipisci iste numquam debitis excepturi ipsum explicabo magni voluptatum ab labore odio autem vitae in earum quisquam, iure maiores ex quos qui aperiam nihil enim eum! Quis excepturi iusto optio pariatur quibusdam non, vero illum minima sunt fugit consequatur harum perferendis incidunt ipsa tenetur labore.quisquam.'

  }
]
</script>

<style scoped>
.hero-image {
  height: 50vh;
  /* always scale the image to the appropriate size of your screen */
  background-size: cover;
  background-image: url('https://images.unsplash.com/photo-1542181961-9590d0c79dab?q=80&w=1470&auto=format&fit=crop&ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D');
  background-position: center;
  /* keeps the image fixed while scrolling , neat effect. */
  background-attachment: fixed;
}
</style>