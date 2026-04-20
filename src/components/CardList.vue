<script setup>
import { ref } from 'vue'
import CardItem from './CardItem.vue'

const items = ref([
  {
    id: 1,
    title: 'Мужские Кроссовки Nike Blazer Mid Suede',
    price: 12990,
    imageUrl: '/sneakers/sneakers-1.jpg',
    isFavorite: false,
    isAdded: false,
  },
  {
    id: 2,
    title: 'Мужские Кроссовки Nike Air Max 270',
    price: 15600,
    imageUrl: '/sneakers/sneakers-2.jpg',
    isFavorite: true,
    isAdded: false,
  },
  {
    id: 3,
    title: 'Мужские Кроссовки Nike Air Force 1',
    price: 13500,
    imageUrl: '/sneakers/sneakers-3.jpg',
    isFavorite: false,
    isAdded: true,
  },
  {
    id: 4,
    title: 'Кроссовки Puma X Ray 2 Square',
    price: 9800,
    imageUrl: '/sneakers/sneakers-4.jpg',
    isFavorite: false,
    isAdded: false,
  },
  {
    id: 5,
    title: 'Кроссовки Under Armour Curry 8',
    price: 17400,
    imageUrl: '/sneakers/sneakers-5.jpg',
    isFavorite: false,
    isAdded: false,
  },
  {
    id: 6,
    title: 'Кроссовки Nike Kyrie 7',
    price: 11200,
    imageUrl: '/sneakers/sneakers-6.jpg',
    isFavorite: true,
    isAdded: true,
  },
  {
    id: 7,
    title: 'Кроссовки Jordan Air Jordan 11',
    price: 10700,
    imageUrl: '/sneakers/sneakers-7.jpg',
    isFavorite: false,
    isAdded: false,
  },
  {
    id: 8,
    title: 'Кроссовки Nike LeBron 18',
    price: 16400,
    imageUrl: '/sneakers/sneakers-8.jpg',
    isFavorite: false,
    isAdded: false,
  },
])

const toggleFavorite = (item) => {
  item.isFavorite = !item.isFavorite
}

const toggleAdd = (item) => {
  item.isAdded = !item.isAdded
}
</script>

<template>
  <ul class="grid grid-cols-4 gap-5">
    <CardItem
      v-for="item in items"
      :key="item.id"
      v-bind="item"
      :onClickFavorite="() => toggleFavorite(item)"
      :onClickAdd="() => toggleAdd(item)"
    />
  </ul>
</template>
