<script setup>
import Draw from "./Draw.vue";
import CarditemFile from "./CarditemFile.vue";
</script>
<template>
  <div class="fixed top-0 left-0 h-full w-full bg-black z-10 opacity-70"></div>
  <div class="bg-white w-96 h-full fixed right-0 top-0 z-20 p-4">
    <Draw />
    <CarditemFile />
    <div class="flex flex-col gap-5">
      <div class="flex gap-2 justify-between">
        <span>Итого: </span>
        <div class="flex-1 border-b border-dashed"></div>
        <b>123124 сом</b>
      </div>
      <div class="flex gap-2 justify-between">
        <span>Налог: </span>
        <div class="flex-1 border-b border-dashed"></div>
        <b>123124 сом</b>
      </div>
      <button
        class="bg-lime-500 w-full rounded-xl py-3 text-white hover:bg-lime-500 active:bg-lime-700"
      >
        Оформить заказ
      </button>
    </div>
  </div>
</template>
