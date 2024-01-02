<script setup>
defineProps({
    cardImage: String,
    cardTitle: String,
    cardPrice: Number,
    isFavorite: Boolean,
    isAdded: Boolean,
    onClickAdd: Function,
    onClickFavorite: Function,
})
</script>
<template>
    <div class="relative border border-gray-200 rounded-xl overflow-hidden p-4 hover:-translate-y-2 hover:shadow-xl transition cursor-pointer bg-white">
      <div>
        <img :src="isFavorite ? '/like-2.svg' : '/like-1.svg'" alt="like 1" class="absolute top-5 left-5 " @click="onClickFavorite">
        <img :src="cardImage">
        <p class="text-left mt-4 text-sm">{{ cardTitle }}</p>
      </div>
      <div class="flex justify-between mt-3">
        <div class="flex flex-col">
          <span class="text-gray-400">Price</span>
          <span class="text-black font-bold">{{cardPrice}} USD</span>
        </div>
        <img :src="isAdded ? '/checked.svg' : '/plus.svg'" @click="onClickAdd">
      </div>
    </div>
</template>