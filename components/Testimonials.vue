<template>
  <div class="container mx-auto my-24 md:px-6">
    <SectionHeaderCenter title="Don't just take our word for it... Read reviews from our customers" header="Testimonials"
      content="Lorem ipsum dolor sit amet, consectetur adipisicing elit. Quod eos id officiis hic tenetur quae quaerat ad velit ab hic." />
    <section class="mb-32  mt-20 text-center px-5 lg:px-0">
      <div class="grid gap-x-6 md:grid-cols-3 lg:gap-x-12">
        <div class="mb-12 md:mb-0">
          <div class="mb-6 flex justify-center">
            <img src="https://mdbcdn.b-cdn.net/img/Photos/Avatars/img%20(1).jpg"
              class="w-32 rounded-full shadow-lg dark:shadow-black/20" />
          </div>
          <h5 class="mb-2 text-lg font-bold text-[var(--aero)] ">Maria Smantha</h5>
          <p class="mb-4">
            Lorem ipsum dolor sit amet, consectetur adipisicing elit. Quod eos
            id officiis hic tenetur quae quaerat ad velit ab hic.
            <svg xmlns="http://www.w3.org/2000/svg" viewBox="0 96 960 960" class="inline-block w-6">
              <path fill="currentColor"
                d="M580 556h160V396H580v160Zm-360 0h160V396H220v160Zm406 220 80-160H520V336h280v288l-76 152h-98Zm-360 0 80-160H160V336h280v288l-76 152h-98Zm34-300Zm360 0Z" />
            </svg>
          </p>
          <div class="flex gap-2  justify-center text-amber-300">
            <Icon v-for="(i, index) in 4" :key="index" name="ic:round-star" color="text-warning" size="30" />
            <Icon name="ic:round-star-half" color="text-warning" size="30" />
          </div>
        </div>
        <div class="mb-12 md:mb-0">
          <div class="mb-6 flex justify-center">
            <img src="https://mdbcdn.b-cdn.net/img/Photos/Avatars/img%20(2).jpg"
              class="w-32 rounded-full shadow-lg dark:shadow-black/20" />
          </div>
          <h5 class="mb-2 text-lg font-bold text-[var(--aero)] ">Lisa Cudrow</h5>
          <p class="mb-4">
            Ut enim ad minima veniam, quis nostrum exercitationem ullam corporis
            suscipit laboriosam, nisi ut aliquid commodi.
            <svg xmlns="http://www.w3.org/2000/svg" viewBox="0 96 960 960" class="inline-block w-6">
              <path fill="currentColor"
                d="M580 556h160V396H580v160Zm-360 0h160V396H220v160Zm406 220 80-160H520V336h280v288l-76 152h-98Zm-360 0 80-160H160V336h280v288l-76 152h-98Zm34-300Zm360 0Z" />
            </svg>
          </p>
          <div class="flex gap-2  justify-center text-amber-300">
            <Icon v-for="(i, index) in 5" :key="index" name="ic:round-star" color="text-warning" size="30" />
          </div>
        </div>
        <div class="mb-0">
          <div class="mb-6 flex justify-center">
            <img src="https://mdbcdn.b-cdn.net/img/Photos/Avatars/img%20(9).jpg"
              class="w-32 rounded-full shadow-lg dark:shadow-black/20" />
          </div>
          <h5 class="mb-2 text-lg font-bold text-[var(--aero)] ">John Smith</h5>
          <p class="mb-4">
            At vero eos et accusamus et iusto odio dignissimos ducimus qui
            blanditiis praesentium voluptatum deleniti atque corrupti.
            <svg xmlns="http://www.w3.org/2000/svg" viewBox="0 96 960 960" class="inline-block w-6">
              <path fill="currentColor"
                d="M580 556h160V396H580v160Zm-360 0h160V396H220v160Zm406 220 80-160H520V336h280v288l-76 152h-98Zm-360 0 80-160H160V336h280v288l-76 152h-98Zm34-300Zm360 0Z" />
            </svg>
          </p>
          <div class="flex gap-2  justify-center text-amber-300">
            <Icon v-for="(i, index) in 4" :key="index" name="ic:round-star" color="text-warning" size="30" />
            <Icon name="ic:round-star-border" color="text-warning" size="30" />
          </div>
        </div>
     
      </div>
    </section>
  </div>
</template>

<script lang="ts" setup>


</script>

<style></style>