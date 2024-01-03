<script setup>
defineProps({
    cardImage: String,
    cardTitle: String,
    cardPrice: Number,
})
</script>
<template>
    <div class="flex gap-5 mb-5 items-center justify-between border border-gray-200 rounded-xl overflow-hidden p-4 hover:-translate-y-2 hover:shadow-xl transition cursor-pointer bg-white">
        <img :src="cardImage" class="w-32">
        <div class="flex flex-col gap-2">
            <p class="text-left text-md font-bold">{{cardTitle}}</p>
            <p class="text-left text-md text-gray-400 font-bold">{{cardPrice}} USD</p>
        </div>
        <img src="/close.svg">
    </div>
</template>