<script setup>
// import AppDrawer from './components/Cart/AppDrawer.vue'
import AppHeader from './components/AppHeader.vue'
import CardList from './components/CardList.vue'
</script>

<template>
  <!-- <AppDrawer /> -->

  <main class="w-4/5 my-20 mx-auto bg-white rounded-2xl shadow-xl pb-10">
    <AppHeader />

    <section class="p-10">
      <h2 class="text-3xl font-bold mb-10">Все кроссовки</h2>

      <CardList />
    </section>
  </main>
</template>
