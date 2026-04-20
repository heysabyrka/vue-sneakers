<template>
  <div class="flex flex-col gap-4 mt-7">
    <div class="flex flex-col gap-2">
      <div class="flex items-end gap-2">
        <span>Итого:</span>
        <div class="flex-1 border-b border-dashed border-slate-200 mb-1"></div>
        <b class="font-bold">12 990 руб.</b>
      </div>

      <div class="flex items-end gap-2">
        <span>Налог 5%:</span>
        <div class="flex-1 border-b border-dashed border-slate-200 mb-1"></div>
        <b class="font-bold">649.5 руб.</b>
      </div>
    </div>

    <button
      class="mt-4 transition bg-lime-500 w-full rounded-xl py-3 text-white disabled:bg-slate-300 hover:bg-lime-600 active:bg-lime-700 cursor-pointer"
    >
      Оформить заказ
    </button>
  </div>
</template>
