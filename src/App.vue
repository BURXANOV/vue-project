<script setup>
import { onMounted, ref } from "vue";
import axios from "axios";
import Header from "./components/Header.vue";
import CardFile from "./components/CardFile.vue";
import Drawer from "./components/Drawer.vue";
const items = ref([]);
onMounted(async () => {
  try {
    const { data } = await axios.get(
      "https://c45a545190626914.mokky.dev/items"
    );
    items.value = data;
  } catch (error) {
    console.log(error);
  }
});
</script>

<template>
  <div
    class="w-4/5 m-auto mt-20 mb-10 rounded-xl p-5 shadow-xl h-auto bg-white border"
  >
    <Header />
    <!-- <Drawer /> -->
    <div class="flex justify-between items-center p-10">
      <p class="font-semobold mb-8 text-3xl">Все кроссовки</p>
      <div class="flex">
        <select class="mr-2 border p-2 rounded-md outline-none">
          <option class="rounded-sm" value="">По название</option>
          <option value="">по цене</option>
          <option value="">по цене</option>
        </select>
        <div class="relative">
          <img class="absolute left-4 top-3" src="/search.svg" alt="" />
          <input
            class="border rounded-md pl-11 py-2 pr-4 outline-none"
            placeholder="поиск"
            type="text"
          />
        </div>
      </div>
    </div>
    <CardFile :items="items" />
  </div>
</template>

<style></style>
