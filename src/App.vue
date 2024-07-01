<script setup>
import Header from './components/Header.vue'
import Card from './components/Card.vue'
</script>

<template>
  <div class="bg-white rounded-xl h-screen w-4/5 m-auto shadow-xl mt-14">
    <Header />
    <h2 text-3xl fonst-bold mb-10>SNEAKERLAR</h2>
    <div class="grid grid-cols-4">
      <Card />
      <Card />
      <Card />
      <Card />
      <Card />
      <Card />
    </div>
  </div>
</template>
