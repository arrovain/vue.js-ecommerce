<script setup>
import { ref, provide, watch, computed } from 'vue'

import Header from './components/Header.vue'
import CardList from './components/CardList.vue'
import Card from './components/Card.vue'
import Drawer from './components/Drawer.vue'
const cart = ref([])
const drawerOpen = ref(false)

const totalPrice = computed(() => cart.value.reduce((acc, item) => acc + item.price, 0))
const vatPrice = computed(() => Math.round((totalPrice.value * 5) / 100))
const closeDrawer = () => {
  drawerOpen.value = false
}

const openDrawer = () => {
  drawerOpen.value = true
}

const addToCart = (item) => {
  cart.value.push(item)
  item.isAdded = true
}

const removeFromCart = (item) => {
  cart.value.splice(cart.value.indexOf(item), 1)
  item.isAdded = false
}
</script>

<template>
  <div class="bg-white rounded-xl h-screen w-4/5 m-auto shadow-xl mt-14">
    <Header />
    <h2 class="text-3xl font-bold mb-8">SPOR AYAKKABILAR</h2>
  </div>
</template>
