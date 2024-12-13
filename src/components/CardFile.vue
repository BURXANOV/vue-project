<script setup>
import Card from "./Card.vue";

defineProps({
  items: Array,
});
</script>

<template>
  <div class="grid grid-cols-3 gap-4">
    <Card
      v-for="item in items"
      :key="item.id"
      :imageUrl="item.imageUrl"
      :title="item.title"
      :price="item.price"
      :isFavorite="false"
      :isAdded="false"
    />
  </div>
</template>
