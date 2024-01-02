<script setup>
import Header from '@/components/Header.vue'
import CardList from '@/components/CardList.vue'
</script>

<template>
  <div class="w-4/5 m-auto bg-white rounded-xl shadow-xl mt-12 overflow-hidden">
    <Header />

    <div class="p-5">
      <p class="text-xl font-bold mb-5">All products</p>
      
      <CardList />
    </div>
  </div>
</template>

<style scoped>
</style>
