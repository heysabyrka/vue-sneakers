<script setup>
defineProps({
  title: String,
  imageUrl: String,
  price: Number,
  isAdded: Boolean,
  isFavorite: Boolean,
  onClickFavorite: Function,
  onClickAdd: Function,
})
</script>

<template>
  <article
    class="relative bg-white border border-slate-100 rounded-3xl p-8 cursor-pointer transition hover:-translate-y-2 hover:shadow-xl"
  >
    <img
      :src="isFavorite ? '/like-2.svg' : '/like-1.svg'"
      alt="Like"
      class="absolute top-8 left-8"
      @click="onClickFavorite"
    />

    <img :src="imageUrl" alt="Sneaker" />

    <p class="mt-2 text-slate-700">{{ title }}</p>

    <div class="flex justify-between items-center mt-5">
      <div class="flex flex-col">
        <span class="text-slate-400 uppercase text-[11px] font-bold">Цена:</span>
        <b class="text-sm">{{ price }} руб.</b>
      </div>

      <button
        class="flex items-center justify-center w-8 h-8 border border-slate-200 rounded-lg hover:border-slate-300 transition"
        @click="onClickAdd"
      >
        <img :src="isAdded ? '/checked.svg' : '/plus.svg'" alt="Plus" />
      </button>
    </div>
  </article>
</template>
