<script setup>
import Header from './components/Header.vue'
import CardList from './components/CardList.vue'
import Card from './components/Card.vue'
import Drawer from './components/Drawer.vue'
</script>

<template>
  <div class="bg-white rounded-xl h-screen w-4/5 m-auto shadow-xl mt-14">
    <Header />
    <h2 class="text-3xl font-bold mb-8">SNEAKERLAR</h2>
    <CardList />
  </div>
</template>
