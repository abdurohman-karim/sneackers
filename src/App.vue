<script setup>
import Header from '@/components/Header.vue'
import CardList from '@/components/CardList.vue'
// import Drawer from '@/components/Drawer.vue'
</script>

<template>
  <!-- <Drawer /> -->
  <div class="w-4/5 m-auto bg-white rounded-xl shadow-xl mt-12 overflow-hidden">
    <Header />

    <div class="p-5">
      <div class="flex justify-between items-center">
        <p class="text-xl font-bold mb-5">All products</p>
        <div class="flex gap-5">
          <select class="text-sm h-8 border border-gray-300 rounded-lg focus:outline-none focus:ring focus:border-blue ring-gray-200 transition pl-2">
          <option>Name</option>
          <option>Price (low to high)</option>
          <option>Price (high to low)</option>
        </select>
        <div class="relative">
          <input type="text" class="text-sm pl-10 px-2 h-8 border border-gray-300 rounded-lg focus:outline-none focus:ring focus:border-blue ring-gray-200 transition" placeholder="Search">
          <img src="/search.svg" class="absolute top-2 left-3">
        </div>
        </div>
      </div>
      
      <CardList />
    </div>
  </div>
</template>

<style scoped>
</style>
