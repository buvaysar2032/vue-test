<script setup>
import Card from "./Card.vue";

defineProps({
  items: Array,
});

const emit = defineEmits(['addToFavorite', 'addToCart']);
</script>

<template>
  <div class="grid grid-cols-4 gap-5">
    <Card
        v-for="item in items"
        :key="item.id"
        :id="item.id"
        :title="item.title"
        :imageUrl="item.imageUrl"
        :price="item.price"
        :isFavorite="item.isFavorite"
        :isAdded="item.isAdded"
        :onClickAdd="() => emit('addToCart', item)"
        :onClickFavorite="() => emit('addToFavorite', item)"
    />
  </div>
</template>

<style scoped>

</style>