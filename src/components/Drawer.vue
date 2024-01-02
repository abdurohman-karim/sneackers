<script setup>
import DrawerCardList from './DrawerCardList.vue'
</script>
<template>
    <div class="fixed top-0 left-0 w-full h-full bg-black bg-opacity-60 z-50">
        <div class="bg-white w-1/4 h-full float-right shadow-xl p-5">
            <h2 class="text-2xl font-bold mb-5 text-gray-700">Cart</h2>
            <DrawerCardList />
        </div>
    </div>
</template>