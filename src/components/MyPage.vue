<script setup>
defineProps({
  title: String,
  price: Number,
});
</script>
<template>
  <div class="border rounded-sm m-5 p-5">
    <h2>Товар:{{ title }}</h2>
    <h3>цена:{{ price }}</h3>
  </div>
</template>
<style scoped></style>
