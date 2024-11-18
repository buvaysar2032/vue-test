<script setup>
import {inject} from "vue";
import CartItem from "./CartItem.vue";

const {cart, addToCart} = inject('cart');

const onClickRemove = () => {}
</script>

<template>
  <div class="flex flex-col  gap-4">
    <CartItem
        v-for="item in cart"
        :key="item.id"
        :title="item.title"
        :imageUrl="item.imageUrl"
        :price="item.price"
    />
  </div>
</template>

<style scoped>

</style>