<template>
  <main class="  ">
    <PageHeader title="Our Special Menu" content="  Lorem ipsum dolor sit amet, consectetur adipisicing elit. Consequuntur, corporis similique. Maxime corrupti possimus
      exercitationem." />
    <div class="lg:p-20">
      <section v-for="(section, index) in sections" :key="section.title"
        class="bg-base-100 my-12 flex flex-col lg:flex-row space-y-4 p-8">
        <div class="lg:flex">
          <div :class="index % 2 === 0 ? ' order-1' : ' order-0'" class="flex lg:w-1/2 items-center justify-center">
            <img :src="section.image" alt="about image">
          </div>
          <article :class="index % 2 === 1 ? ' order-1' : ' order-0'"
            class="text-center flex lg:w-1/2 flex-col space-y-6 p-10">
            <h2 class="text-xl lg:text-2xl font-serif text-orange-300 ">
              {{ section.price }}
            </h2>
            <h1 class="mb-0 font-serif text-2xl lg:text-3xl font-bold">
              {{ section.title }}
            </h1>
            <IconDivider />
            <p class="leading-8 font-sans text-gray-600">
              {{ section.content }}
            </p>
          </article>
        </div>
      </section>
      <section>
        <div class="flex flex-col items-center  justify-center  my-10 lg:my-20">
          <Icon name="ep:dessert" class="text-8xl text-orange-300 mb-8 drop" />
          <div class=" text-3xl lg:text-4xl font-serif">More Sweets Menu</div>
          <div class="w-full my-5">
            <IconDivider />
          </div>
        </div>
        <div class=" px-4 lg:px-32">
          <ul>
            <li v-for="menuItem in menuItems"
              class="flex flex-col lg:flex-row items-center justify-between w-full border-b p-4 hover:shadow-md  transition-all duration-200">
              <div class="flex flex-col items-center justify-between w-4/5">
                <div class="flex flex-col items-start   w-full">
                  <h1 class="text-xl lg:text-2xl font-serif  font-bold mb-4">{{ menuItem.title }}</h1>
                  <h2 class="text-2xl font-serif text-orange-300 lg:hidden mb-4 ">
                    {{ menuItem.price }}
                  </h2>
                  <p class="text-gray-600 font-sans">{{ menuItem.content }}</p>
                </div>
              </div>
              <v-divider :thickness="1" class="border-opacity-100" vertical></v-divider>
              <div class="flex   justify-center w-1/5">
                <h2 class="text-2xl font-serif text-orange-300 hidden lg:block ">
                  {{ menuItem.price }}
                </h2>
              </div>
            </li>
          </ul>
        </div>
      </section>
      <section class=" my-16 lg:my-32">
        <div class="flex flex-col items-center  justify-center  my-10 lg:my-20">
          <Icon name="simple-icons:coffeescript" class="text-8xl text-orange-300 mb-8 drop" />
          <div class="text-3xl lg:text-4xl font-serif">Coffee & Drinks</div>
          <div class="w-full my-5">
            <IconDivider />
          </div>
        </div>
        <div class=" px-4 lg:px-32">
          <ul>
            <li v-for="menuItem in menuItems"
              class="flex flex-col lg:flex-row items-center justify-between w-full border-b p-4 hover:shadow-md  transition-all duration-200">
              <div class="flex flex-col items-center justify-between w-4/5">
                <div class="flex flex-col items-start   w-full">
                  <h1 class="text-xl lg:text-2xl font-serif  font-bold mb-4">{{ menuItem.title }}</h1>
                  <h2 class="text-2xl font-serif text-orange-300 lg:hidden mb-4 ">
                    {{ menuItem.price }}
                  </h2>
                  <p class="text-gray-600 font-sans">{{ menuItem.content }}</p>
                </div>
              </div>
              <v-divider :thickness="1" class="border-opacity-100" vertical></v-divider>
              <div class="flex   justify-center w-1/5">
                <h2 class="text-2xl font-serif text-orange-300 hidden lg:block ">
                  {{ menuItem.price }}
                </h2>
              </div>
            </li>
          </ul>
        </div>
      </section>
    </div>
    <div class="my-20">
      <CallToAction />
    </div>
  </main>
</template>

<script lang="ts" setup>
import CallToAction from '~/components/Globals/CallToAction.vue';
import IconDivider from '~/components/Globals/IconDivider.vue';
import PageHeader from '~/components/Globals/PageHeader.vue';


const sections = [
  {
    title: 'Lorem ipsum',
    price: '$2.79',
    image:
      'https://images.unsplash.com/photo-1447078806655-40579c2520d6?q=80&w=1470&auto=format&fit=crop&ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D',
    content: ` Lorem ipsum dolor sit, amet consectetur adipisicing elit. Dolorum, ea consequuntur quis cupiditate facere labore natus autem similique voluptatum quidem tempore nisi, laboriosam, quo magni.`,
  },
  {
    title: 'Lorem ipsum',
    price: '$3.25',
    image:
      'https://images.unsplash.com/photo-1587314168485-3236d6710814?q=80&w=1378&auto=format&fit=crop&ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D',
    content:
      ' Lorem ipsum dolor sit, amet consectetur adipisicing elit. Dolorum, ea consequuntur quis cupiditate facere labore natus autem similique voluptatum quidem tempore nisi, laboriosam, quo magni.',
  },
  {
    title: 'Lorem ipsum',
    price: '$1.45',
    image:
      'https://images.unsplash.com/photo-1533134242443-d4fd215305ad?q=80&w=1470&auto=format&fit=crop&ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D',
    content: ` Lorem ipsum dolor sit, amet consectetur adipisicing elit. Dolorum, ea consequuntur quis cupiditate facere labore natus autem similique voluptatum quidem tempore nisi, laboriosam, quo magni.`,
  },
  {
    title: 'Lorem ipsum',
    price: '$8.75',
    image:
      'https://images.unsplash.com/photo-1614822283221-92abecbbc659?q=80&w=1470&auto=format&fit=crop&ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D',
    content: ` Lorem ipsum dolor sit, amet consectetur adipisicing elit. Dolorum, ea consequuntur quis cupiditate facere labore natus autem similique voluptatum quidem tempore nisi, laboriosam, quo magni.`,
  },
]

const menuItems = [
  {
    title: 'Lorem ipsum',
    price: '$8.79',
    content: 'Lorem ipsum dolor sit, amet consectetur adipisicing elit. Dolorum, ea consequuntur quis cupiditate facere labore natus autem similique voluptatum quidem tempore nisi.',
  },
  {
    title: 'Aliquam volutpat',
    price: '$9.25',
    content: 'Lorem ipsum dolor sit, amet consectetur adipisicing elit. Dolorum, ea consequuntur quis cupiditate facere labore natus autem similique voluptatum quidem tempore nisi.',
  },
  {
    title: 'Morbin semquis',
    price: '$10',
    content: 'Lorem ipsum dolor sit, amet consectetur adipisicing elit. Dolorum, ea consequuntur quis cupiditate facere labore natus autem similique voluptatum quidem tempore nisi.',
  },
  {
    title: 'facere labore',
    price: '$7.89',
    content: 'Lorem ipsum dolor sit, amet consectetur adipisicing elit. Dolorum, ea consequuntur quis cupiditate facere labore natus autem similique voluptatum quidem tempore nisi.',
  },
  {
    title: 'cupiditate',
    price: '$9.50',
    content: 'Lorem ipsum dolor sit, amet consectetur adipisicing elit. Dolorum, ea consequuntur quis cupiditate facere labore natus autem similique voluptatum quidem tempore nisi.',
  },
  {
    title: 'natus autem',
    price: '$10.50',
    content: 'Lorem ipsum dolor sit, amet consectetur adipisicing elit. Dolorum, ea consequuntur quis cupiditate facere labore natus autem similique voluptatum quidem tempore nisi.',
  },
  {
    title: 'dolor sit',
    price: '$6.98',
    content: 'Lorem ipsum dolor sit, amet consectetur adipisicing elit. Dolorum, ea consequuntur quis cupiditate facere labore natus autem similique voluptatum quidem tempore nisi.',
  },
]
</script>

<style scoped></style>