<script setup lang="ts">
import { defineProps } from 'vue'

interface IconListItem {
  icon: string
  text: string
  iconColor?: string // Added the iconColor prop
}

const props = defineProps({
  items: {
    type: Array as () => IconListItem[],
    required: true,
  },
  iconSize: {
    type: String,
    default: '24px',
  },
})
</script>

<template>
  <ul class="icon-list">
    <li v-for="(item, index) in items" :key="index" class="icon-list-item">
      <div class="icon-wrapper">
        <Icon :name="item.icon" :style="{ fontSize: iconSize, color: item.iconColor }" class="" />
      </div>
      <div class="text-wrapper">
        <slot :name="`item-${index}`">
          {{ item.text }}
        </slot>
      </div>
    </li>
  </ul>
</template>

<style scoped>
.icon-list {
  list-style: none;
  padding: 0;
}

.icon-list-item {
  display: flex;
  align-items: center;
  margin-bottom: 10px;
}

.icon-wrapper {
  margin-right: 10px;
}

.text-wrapper {
  flex: 1;
}
</style>
