<script setup>
import { ref } from 'vue'
import CartItem from './CartItem.vue'

const items = ref([
  {
    id: 1,
    title: 'Мужские Кроссовки Nike Air Max 270',
    price: 12990,
    imageUrl: '/sneakers/sneakers-1.jpg',
  },
  {
    id: 2,
    title: 'Мужские Кроссовки Nike Air Force 1',
    price: 15490,
    imageUrl: '/sneakers/sneakers-2.jpg',
  },
])
</script>

<template>
  <ul class="flex flex-col flex-1 gap-4 overflow-y-auto">
    <CartItem v-for="item in items" :key="item.id" v-bind="item" />
  </ul>
</template>
