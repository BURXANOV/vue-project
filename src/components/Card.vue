<script setup>
defineProps({
  imageUrl: String,
  title: String,
  price: Number,
  isFavorite: Boolean,
  isAdded: Boolean,
  onClickAdded: Function,
  onClickFavorite: Function,
});
</script>

<template>
  <div
    class="relative border m-10 border-slate-100 rounded-xl cursor-pointer p-4 hover:-translate-y-2 transition hover:shadow-xl"
  >
    <img
      :src="!isFavorite ? '/like-1.svg' : '/like-2.svg'"
      class="absolute m-5 top-0 left-0"
      alt="like icon"
      @click="onClickFavorite"
    />
    <img :src="imageUrl" alt="Product Image" class="w-full h-auto" />
    <p class="mt-4 text-lg font-semibold">{{ title }}</p>
    <div class="flex justify-between items-center mt-5">
      <div class="flex flex-col">
        <span class="text-sm text-gray-500">Цена:</span>
        <b class="text-xl">{{ price }} сом</b>
      </div>
      <img
        :src="!isAdded ? '/plus.svg' : '/checked.svg'"
        width="34"
        height="34"
        alt="Add Icon"
        class="w-6 h-6"
        @click="onClickAdded"
      />
    </div>
  </div>
</template>
