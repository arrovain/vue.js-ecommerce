<script setup>
defineProps({
  imageUrl: String,
  title: String,
  price: Number,
  isFavorite: Boolean,
  isAdded: Boolean,
  onClickAdd: Function,
  onClickFavorite: Function
})
</script>

<template>
  <div class="bg-white rounded-xl h-screen w-4/5 m-auto shadow-xl mt-14">
    <Header />
    <div>
      <div
        class="relative m-10 border border-slate-100 rounded-2xl p-8 cursor-pointer transition hover:translate-y-2 hover:shadow-xl"
      >
        <img
          src="/like-1.svg"
          alt="Like 1"
          class="absolute top-0 left-0"
          @click="onClickFavorite"
        />
        <img :src="imageUrl" alt="Like 1" />
        <p>{{ title }}</p>
        <div class="flex justify-between mt-5">
          <div class="flex flex-col">
            <span>{{ price }}</span>
          </div>
          <img @click="onClickAdd" :src="isAdded ? '/plus.svg' : '/checked.svg'" alt="Plus" />
        </div>
      </div>
    </div>
  </div>
</template>
