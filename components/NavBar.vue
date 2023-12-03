<script setup lang="ts">
import { onBeforeUnmount, onMounted, ref } from 'vue'
import Button from './Globals/Button.vue'

const navTransform = ref('translateY(0)')
const Y = ref(0)
let lastScrollPosition = 0

const route = useRoute()
route.path

function handleScroll() {
  const scrollY = window.scrollY;


  Y.value = scrollY

  // Adjust the threshold value (200) based on your specific requirement
  const scrollThreshold = 200;

  navTransform.value =
    scrollY > lastScrollPosition && scrollY > scrollThreshold
      ? 'translateY(-100%)'
      : 'translateY(0)';

  lastScrollPosition = scrollY;
}

function handleIndicator(el: HTMLElement) {
  const indicator = document.querySelector('.nav-indicator') as HTMLElement
  const items = document.querySelectorAll('.nav-item')

  items.forEach((item) => {
    item.classList.remove('active')
    item.removeAttribute('style')
  })

  indicator.style.width = `${el.offsetWidth}px`
  indicator.style.left = `${el.offsetLeft}px`

  const activeColor = el.getAttribute('active-color')
  if (activeColor !== null) {
    indicator.style.backgroundColor = activeColor
    el.style.color = activeColor
  }

  el.classList.add('active')
}

interface HTMLElementWithActiveClass extends HTMLElement {
  classList: DOMTokenList & {
    contains(token: string): boolean
  }
}
// Function to setup listeners
function setupIndicatorListeners() {
  const items: NodeListOf<HTMLElement> = document.querySelectorAll('.nav-item')
  const indicator: HTMLElement | null
    = document.querySelector('.nav-indicator')

  items.forEach((item: HTMLElement) => {
    if (item.getAttribute('href') === route.path) {
      item.classList.add('is-active')
      handleIndicator(item)
    }
    item.addEventListener('click', e =>
      handleIndicator(e.target as HTMLElement))
    if ((item as HTMLElementWithActiveClass).classList.contains('is-active'))
      handleIndicator(item)
  })
}

onMounted(() => {
  window.addEventListener('scroll', handleScroll)
  setupIndicatorListeners()
})

onBeforeUnmount(() => {
  window.removeEventListener('scroll', handleScroll)
})







const items = [
  { title: 'Home', href: '/', icon: 'mdi-home-city' },
  { title: 'Our Café', href: '/about', icon: 'mdi-book' },
  { title: 'Gallery', href: '/gallery', icon: 'mdi-apps' },
  { title: 'Menu', href: '/menu', icon: 'mdi-food' },
  { title: 'Contact', href: '/contact', icon: 'mdi-email' },
  { title: 'Shop', href: '/shop', icon: 'mdi-credit-card-plus-outline' },
]


const threshold = ref(200)
</script>
<template>
  <v-app-bar app scroll-behavior="collapse" :scroll-threshold="threshold"
    class="px-4 font-serif transition-color duration-500"
    :class="{ 'bg-white': Y > threshold, 'bg-transparent': Y <= threshold }">
    <template v-slot:prepend>
      <v-menu offset="10">
        <template v-slot:activator="{ props }">
          <v-app-bar-nav-icon v-bind="props"></v-app-bar-nav-icon>
        </template>
        <v-list class="w-full bg-red-400" color="orange-lighten-4">
          <v-list-item v-for="(item, i) in items" :key="i" :value="item" color="primary">
            <NuxtLink :to="item.href">
              <div class="flex space-x-4 my-5">
                <v-icon :icon="item.icon" size="x-large"></v-icon>
                <v-list-item-title v-text="item.title" class="!text-5xl"></v-list-item-title>
              </div>
            </NuxtLink>
          </v-list-item>
        </v-list>
      </v-menu>
    </template>
    <v-toolbar-title>Lorem Ipsum's Café</v-toolbar-title>
    <v-spacer></v-spacer>
    <ul class="gap-4 relative hidden lg:flex">
      <li v-for="(item, index) in items" :key="index">
        <nuxt-link :to="item.href" class="nav-item" exact-active-class="active text-orange-300 drop-shadow-sm ">
          {{ item.title }}
        </nuxt-link>
      </li>
      <div class="nav-indicator"></div>
    </ul>
  </v-app-bar>
</template>

<style scoped>
.nav-item {
  @apply transition-all duration-300 ease-in-out relative p-2 text-xl;
}

.nav-item:before {
  content: "";
  position: absolute;
  bottom: -6px;
  left: 0;
  width: 100%;
  height: 4px;
  background-color: rgba(253, 187, 116, 0.432);
  border-radius: 8px 8px 0 0;
  opacity: 0;
  transition: 0.3s;
}

.nav-item:not(.active):hover:before {
  opacity: 1;
  bottom: 0;
}




.nav-indicator {
  position: absolute;
  left: 0;
  bottom: -6px;
  height: 4px;
  transition: 0.4s;
  background-color: rgb(253 186 116);

  z-index: 999999;
  border-radius: 8px 8px 0 0;
}

.nav-indicator.active {
  transform: translateX(100%);
}

@media (max-width: 580px) {
  .nav {
    overflow: auto;
  }
}
</style>
