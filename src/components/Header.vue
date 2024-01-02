<template>
    <header class="flex justify-between items-center border-b p-4">
      <div class="flex justify-between items-center">
        <img src="/logo.png" alt="Logo" class="w-10 mr-4">
        <div>
          <h2 class="font-bold uppercase text-xl">Vue Sneakers</h2>
          <p class="text-gray-400">Sneakers shop</p>
        </div>
      </div>
      <ul class="flex items-center justify-between gap-10">
          <li class="flex cursor-pointer text-sm text-gray-400 gap-2 hover:text-black">
            <img src="/cart.svg" alt="cart">
            <span>1200 usd</span>
          </li>
          <li class="flex cursor-pointer text-sm text-gray-400 gap-2 hover:text-black">
            <img src="/heart.svg" alt="cart">
            <span>Saved</span>
          </li>
          <li class="flex cursor-pointer text-sm text-gray-400 gap-2 hover:text-black">
            <img src="/profile.svg" alt="cart">
            <span>Profile</span>
          </li>
        </ul>
    </header>
</template>
