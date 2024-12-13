<script setup>
import Card from "./Card.vue";
</script>

<template>
  <div class="grid grid-cols-3 gap-4">
    <Card
      imageUrl="/sneakers/sneakers-1.jpg"
      title="Кроссовки Puma X Aka Boku Future Rider"
      :price="123"
      :isFavorite="false"
      :isAdded="true"
    />
  </div>
</template>
