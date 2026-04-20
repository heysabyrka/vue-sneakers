<script setup>
import { ref } from 'vue'
// import AppDrawer from './components/Cart/AppDrawer.vue'
import AppHeader from './components/AppHeader.vue'
import CardList from './components/CardList.vue'

const sortBy = ref('')
</script>

<template>
  <!-- <AppDrawer /> -->

  <main class="w-4/5 my-20 mx-auto bg-white rounded-2xl shadow-xl pb-10">
    <AppHeader />

    <section class="p-10">
      <div class="flex justify-between items-center mb-10">
        <h2 class="text-3xl font-bold">Все кроссовки</h2>

        <div class="flex gap-4">
          <select
            v-model="sortBy"
            :class="[
              'py-2 px-3 border border-slate-200 rounded-md outline-none bg-white transition focus:border-gray-400',
              sortBy ? 'text-black' : 'text-slate-400',
            ]"
          >
            <option value="" disabled>Сортировка</option>
            <option value="name" class="text-black">По названию</option>
            <option value="price_asc" class="text-black">По цене (дешевые)</option>
            <option value="price_desc" class="text-black">По цене (дорогие)</option>
          </select>

          <div class="relative text-slate-400 focus-within:text-gray-600">
            <img class="absolute left-4 top-3 opacity-30" src="/search.svg" alt="Search" />
            <input
              type="text"
              placeholder="Поиск..."
              class="border border-slate-200 rounded-md py-2 pl-11 pr-4 outline-none text-black placeholder:text-slate-400 focus:border-gray-400 transition"
            />
          </div>
        </div>
      </div>

      <CardList />
    </section>
  </main>
</template>
