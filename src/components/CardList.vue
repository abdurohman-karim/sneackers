<script setup>
import Card from './Card.vue'

defineProps({
    items: Array,
})

const onClickAdd = () => {
    alert('Добавлено в корзину')
}
</script>

<template>
    <div class="grid lg:grid-cols-4 md:grid-cols-3 sm:grid-cols-1 gap-5">
        <Card  v-for="item in items" :key="item.id" :cardImage="item.imageUrl" :cardTitle="item.name" :cardPrice="Number(item.price)" :onClickAdd="onClickAdd" />
    </div>
</template>