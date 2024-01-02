<script setup>
import Card from './Card.vue'

const onClickAdd = () => {
    alert('Добавлено в корзину')
}
</script>

<template>
    <div class="grid grid-cols-4 gap-5">
        <Card cardImage="/sneakers/sneakers-1.jpg" cardTitle="Мужские Кроссовки Nike Blazer Mid Suede" :cardPrice="200" :onClickAdd="onClickAdd" />
    </div>
</template>