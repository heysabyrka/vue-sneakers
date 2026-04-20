<script setup>
const menuItems = [
  { name: '1205 руб.', icon: '/cart.svg', alt: 'Cart' },
  { name: 'Закладки', icon: '/heart.svg', alt: 'Favorites' },
  { name: 'Профиль', icon: '/profile.svg', alt: 'Profile' },
]
</script>

<template>
  <header class="flex justify-between border-b border-slate-200 px-10 py-8">
    <div class="flex items-center gap-4">
      <img src="/logo.png" alt="Vue Sneakers Logo" class="w-10" />
      <div>
        <h1 class="text-xl font-bold uppercase text-black">Vue Sneakers</h1>
        <p class="text-slate-400">Магазин лучших кроссовок</p>
      </div>
    </div>

    <nav>
      <ul class="flex items-center gap-10">
        <li
          v-for="item in menuItems"
          :key="item.name"
          class="flex items-center cursor-pointer gap-3 text-gray-500 hover:text-black transition-all hover:-translate-y-0.5"
        >
          <img :src="item.icon" :alt="item.alt" />
          <span class="font-medium">{{ item.name }}</span>
        </li>
      </ul>
    </nav>
  </header>
</template>
