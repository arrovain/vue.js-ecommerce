<script setup>
import Card from './Card.vue'

const onClickAdd = () => {
  alert('eklendi')
}
</script>

<template>
  <div class="grid grid-cols-4 gap-5">
    <Card
      title="Nike Blazer Mid"
      imageUrl="/sneakers/sneakers-1.jpg"
      :price="2850"
      :isFavorite="false"
      :onClickAdd="onClickAdd"
      :isAdded="true"
    />
    <Card />
    <Card />
    <Card />
    <Card />
    <Card />
  </div>
</template>
