<!-- eslint-disable vue/multi-word-component-names -->
<script setup>
import DrawerCardList from './DrawerCardList.vue'
</script>
<template>
    <div class="fixed top-0 left-0 w-full h-full bg-black bg-opacity-60 z-50">
        <div class="flex flex-col justify-between bg-white w-1/4 h-full float-right shadow-xl p-5">
            <div class="flex flex-col">
                <h2 class="text-2xl font-bold mb-5 text-gray-700">Cart</h2>
                <DrawerCardList />
            </div>

            <div class="flex flex-col gap-4">
                <div class="flex justify-between mt-5 gap-2">
                    <span class="text-gray-400">Total:</span>
                    <div class="flex-1 border-b border-gray-300 border-dashed"></div>
                    <span class="text-gray-500 font-bold">1200$</span>
                </div>
                <div class="flex justify-between mt-5 gap-2">
                    <span class="text-gray-400">Discount 5%:</span>
                    <div class="flex-1 border-b border-gray-300 border-dashed"></div>
                    <span class="text-gray-500 font-bold">50$</span>
                </div>
                <button disabled class="bg-lime-500 disabled:bg-gray-300 mt-3 text-white py-2 rounded-lg text-xl hover:bg-lime-600 transition">Checkout</button>
            </div>
        </div>
    </div>
</template>