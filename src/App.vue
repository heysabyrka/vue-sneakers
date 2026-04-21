<script setup>
// import AppDrawer from './components/Cart/AppDrawer.vue'
import AppHeader from './components/IconAppHeader.vue'
import CardList from './components/CardList.vue'
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
            class="py-2 px-3 border border-slate-200 rounded-md outline-none bg-white focus:border-gray-400 transition"
          >
            <option>По названию</option>
            <option>По цене (дешевые)</option>
            <option>По цене (дорогие)</option>
          </select>

          <div class="relative">
            <img class="absolute left-4 top-3" src="/search.svg" alt="Search" />
            <input
              type="text"
              placeholder="Поиск..."
              class="border border-slate-200 rounded-md py-2 pl-11 pr-4 outline-none focus:border-gray-400 transition"
            />
          </div>
        </div>
      </div>

      <CardList />
    </section>
  </main>
</template>
