<script setup>
defineProps({
  imageUrl: String
})
</script>

<template>
  <div class="bg-white rounded-xl h-screen w-4/5 m-auto shadow-xl mt-14">
    <Header />
    <div>
      <div
        class="relative m-10 border border-slate-100 rounded-2xl p-8 cursor-pointer transition hover:translate-y-2 hover:shadow-xl"
      >
        <img src="/like-1.svg" alt="Like 1" class="absolute top-0 left-0" />
        <img src="/sneakers/sneakers-1.jpg" alt="Like 1" />
        <p>Nike Blazer Mid Suede</p>
        <div class="flex justify-between mt-5">
          <div class="flex flex-col">
            <span>2250TL</span>
          </div>
          <img src="/plus.svg" alt="Plus" />
        </div>
      </div>
    </div>
  </div>
</template>
