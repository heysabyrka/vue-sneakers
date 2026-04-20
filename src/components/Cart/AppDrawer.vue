<script setup>
import DrawerHead from './DrawerHead.vue'
import CartItemList from './CartItemList.vue'
import CartFooter from './CartFooter.vue'
</script>

<template>
  <div class="fixed top-0 left-0 w-full h-full bg-black opacity-70 z-10" />
  <aside class="bg-white w-96 h-full fixed top-0 right-0 z-20 p-8 flex flex-col">
    <DrawerHead />
    <CartItemList />
    <CartFooter />
  </aside>
</template>
