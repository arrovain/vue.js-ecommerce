<script setup></script>

<template>
  <div className="bg-white rounded-xl h-screen w-4/5 m-auto shadow-xl mt-14 ">
    <header class="flex justify-between border-b border-slate-300 px-10 py-8">
      <div class="flex items-center gap-4">
        <img src="/logo.png" alt="logo" class="w-10" />
        <div>
          <h2 class="text-xl font-bold uppercase">İcme Sneakers</h2>
          <p class="text-slate-500">Best seller sneakers</p>
        </div>
      </div>

      <ul class="flex items-center gap-10">
        <li class="flex items-center gap-3 text-gray-500 hover:text-black">
          <img src="/cart.svg" alt="Cart" /> <b>sepet</b>
        </li>
        <li class="flex items-center gap-3 text-gray-500 hover:text-black">
          <img src="/heart.svg" alt="Cart" /> <span>favoriler</span>
        </li>
        <li class="flex items-center gap-3 text-gray-500 hover:text-black">
          <img src="/profile.svg" alt="Cart" /> <span>hesabım</span>
        </li>
      </ul>
    </header>

    <h1>blog</h1>
  </div>
</template>
