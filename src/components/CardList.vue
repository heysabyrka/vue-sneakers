<script setup>
import { onMounted, ref } from 'vue'
import axios from 'axios'

import CardItem from './CardItem.vue'

const items = ref([])

const toggleFavorite = (item) => {
  item.isFavorite = !item.isFavorite
}

const toggleAdd = (item) => {
  item.isAdded = !item.isAdded
}

onMounted(async () => {
  try {
    const { data } = await axios.get('https://e5dc569b98392dff.mokky.dev/items')
    items.value = data
  } catch (error) {
    console.error('Ошибка при загрузке данных:', error)
  }
})
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
