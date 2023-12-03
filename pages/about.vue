<template>
  <main>
    <v-sheet class="p-20">
      <v-carousel>
        <v-carousel-item src="https://themes.muffingroup.com/be/cafe2/wp-content/uploads/2017/09/home_cafe2_ourcafe3.jpg"
          cover></v-carousel-item>
        <v-carousel-item src="https://themes.muffingroup.com/be/cafe2/wp-content/uploads/2017/09/home_cafe2_ourcafe3.jpg"
          cover></v-carousel-item>
        <v-carousel-item src="https://themes.muffingroup.com/be/cafe2/wp-content/uploads/2017/09/home_cafe2_ourcafe2.jpg"
          cover></v-carousel-item>
      </v-carousel>
      <div class="flex flex-col items-center  justify-center  my-10 lg:my-20">
        <Icon name="pepicons-print:flower-bud" class="text-8xl text-orange-300 mb-10" />
        <div class="text-4xl font-serif">A history of our Café </div>
        <div class="w-full my-5">
          <IconDivider />
        </div>
      </div>
      <div class="flex   my-10 lg:my-20">
        <div class="text-4xl  font-serif w-1/2 p-10  leading-10">
          Lorem ipsum dolor sit amet, consectetur adipisicing elit. Nemo necessitatibus ex, minima quo magnam in dolore
          possimus voluptas dicta deleniti.
        </div>
        <div class=" w-1/2 p-10  leading-8"> <strong class="text-8xl  dancing-script text-orange-300">L </strong>orem ipsum
          dolor sit amet
          consectetur adipisicing elit. Fugit ea fuga ducimus pariatur ullam. Earum iste laboriosam fugit sapiente et
          aspernatur perspiciatis assumenda adipisci enim, molestias voluptas officia modi sint maiores hic tenetur optio
          harum, consectetur sunt quae quaerat. Tempora inventore modi excepturi molestiae enim, consectetur numquam odit
          perspiciatis velit architecto dignissimos voluptate quo corporis tenetur ad distinctio aliquam atque saepe quia
      
          iure quae sunt inventore earum ducimus porro quis quasi nihil totam eligendi quisquam. Quasi illo, adipisci iste
          numquam debitis excepturi ipsum explicabo magni voluptatum ab labore odio autem vitae in earum quisquam, iure
          maiores ex quos qui aperiam nihil enim eum! Quis excepturi iusto optio pariatur quibusdam non, vero illum minima
          sunt fugit consequatur harum perferendis incidunt ipsa tenetur labore.quisquam. </div>
      </div>
      <div class="flex   my-10 lg:my-20">
        <div class="text-4xl  font-serif w-1/2 p-10  leading-10">
          Lorem ipsum dolor sit amet, consectetur adipisicing elit Nemo necessitatibus ex.
        </div>
        <div class=" w-1/2 p-10  leading-8"> <strong class="text-8xl dancing-script text-orange-300">I </strong>orem ipsum
          dolor sit amet
          consectetur adipisicing elit. Fugit ea fuga ducimus pariatur ullam. Earum iste laboriosam fugit sapiente et
          aspernatur perspiciatis assumenda adipisci enim, molestias voluptas officia modi sint maiores hic tenetur optio
          harum, consectetur sunt quae quaerat. Tempora inventore modi excepturi molestiae enim, consectetur numquam odit
          perspiciatis velit architecto dignissimos voluptate quo corporis tenetur ad distinctio aliquam atque saepe quia
          doloribus vitae ea dolores at? Esse iure nemo sunt incidunt adipisci quaerat sapiente, voluptatum eveniet
          quisquam vitae magnam vel rerum autem? Doloremque facere nam ut ab dolor ea quisquam iste libero perferendis in,
          impedit sit amet fugiat optio aut. Perspiciatis cupiditate culpa, minus voluptatum, dolorum non a molestiae sed
          iure quae sunt inventore earum ducimus porro quis quasi nihil totam eligendi quisquam. Quasi illo, adipisci iste
          numquam debitis excepturi ipsum explicabo magni voluptatum ab labore odio autem vitae in earum quisquam, iure
          maiores ex quos qui aperiam nihil enim eum! Quis excepturi iusto optio pariatur quibusdam non, vero illum minima
          sunt fugit consequatur harum perferendis incidunt ipsa tenetur labore.quisquam. </div>
      </div>



         <div class="flex   my-10 lg:my-20">
          <div class="text-4xl  font-serif w-1/2 p-10  leading-10">
           Consectetur adipisicing elit Nemo necessitatibus ex.
          </div>
          <div class=" w-1/2 p-10  leading-8"> <strong class="text-8xl dancing-script text-orange-300">C </strong>orem ipsum
            dolor sit amet
            consectetur adipisicing elit. Fugit ea fuga ducimus pariatur ullam. Earum iste laboriosam fugit sapiente et
            aspernatur perspiciatis assumenda adipisci enim, molestias voluptas officia modi sint maiores hic tenetur optio
            harum, consectetur sunt quae quaerat. Tempora inventore modi excepturi molestiae enim, consectetur numquam odit
            perspiciatis velit architecto dignissimos voluptate quo corporis tenetur ad distinctio aliquam atque saepe quia
            doloribus vitae ea dolores at. </div>
        </div>
      <div class="flex flex-col items-center  justify-center  my-10 lg:my-20">
        <Icon name="pepicons-print:flower-bud" class="text-8xl text-orange-300 mb-10" />
        <div class="text-4xl font-serif"> Lorem ipsum dolor sit. </div>
        <div class="w-full pt-8">
          <IconDivider />
        </div>
        <div class="w-2/3 text-center my-8">
          <p>Lorem, ipsum dolor sit amet consectetur adipisicing elit. Amet, iure optio rem nihil placeat laboriosam id
            tempora aliquid quam, maxime eligendi dolorem eum quisquam eius!</p>
        </div>
        <div class=" flex flex-col space-y-5 items-center justify-center ">
          <a href="/contact">
            <v-btn size="x-large" color="orange-lighten-3">Contact</v-btn>
          </a>
          <a href="/shop">
            <v-btn size="x-large" variant="outlined" color="orange-lighten-3">Shop</v-btn>
          </a>
        </div>
      </div>
    </v-sheet>
    <div class="hero-image relative border-y-2 border-gray-800">
      <div
        class="absolute -top-8 left-1/2 -translate-x-1/2  bg-black rounded-full p-1 shadow-md border-2 border-orange-300 hover:shadow-xl transition-all duration-150 ">
        <Icon name='ph:flower-lotus' class="text-amber-400 text-6xl" />
      </div>
    </div>
  </main>
</template>

<script lang="ts" setup>
import IconDivider from '~/components/Globals/IconDivider.vue';


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