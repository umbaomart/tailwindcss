<script setup>
import { ref } from 'vue'
import ProductDisplay from './components/ProductDisplay.vue'

const cart = ref([])
const premium = ref(true)

function updateCart(id) {
  cart.value.push(id)
}
</script>

<template>
  <!-- <div class="nav-bar"></div> -->
  <div class="h-[60px] mb-[25px] bg-gradient-to-r from-ocean to-leaf"></div>

  <!-- <div class="cart">Cart({{ cart.length }})</div> -->
  <div class="my-[25px] mx-[100px] p-[30px] border-[1px] border-mist bg-white float-right">Cart({{ cart.length }})</div>
  <product-display :premium="premium" @add-to-cart="updateCart"></product-display>
</template>