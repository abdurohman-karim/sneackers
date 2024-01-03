<script setup>
import { onMounted, ref, watch, reactive } from 'vue'
import axios from 'axios'

import Header from '@/components/Header.vue'
import CardList from '@/components/CardList.vue'
// import Drawer from '@/components/Drawer.vue'

const items = ref([]);

const filters = reactive({
  sortBy: 'name',
  searchQuery: '',
});

const onChangeSelect = (event) =>{
  filters.sortBy = event.target.value
}

const onChangeSearch = (event) =>{
  filters.searchQuery = event.target.value
}

const fetchFavourites = async () => {
  try{
    

    const { data } = await axios.get(`https://bdd9a1e327bffb1a.mokky.dev/items`);
    items.value = data;
  } catch (err) {
    console.log(err);
  }
}

const fetchItems = async () => {
  try{
    const params = {
      sortBy: filters.sortBy,
    }

    if (filters.searchQuery) {
      params.name = `*${filters.searchQuery}*`
    }
    const { data } = await axios.get(`https://bdd9a1e327bffb1a.mokky.dev/items`, { params });
    items.value = data;
  } catch (err) {
    console.log(err);
  }
}
onMounted(fetchItems);
watch(filters, fetchItems);

</script>

<template>
  <!-- <Drawer /> -->
  <div class="w-4/5 m-auto bg-white rounded-xl shadow-xl mt-12 overflow-hidden">
    <Header />

    <div class="p-5">
      <div class="flex justify-between items-center mb-5">
        <p class="text-xl font-bold mb-5">All products</p>
        <div class="flex gap-5">
          <select @change="onChangeSelect" class="text-sm h-8 border border-gray-300 rounded-lg focus:outline-none focus:ring focus:border-blue ring-gray-200 transition pl-2">
          <option value="name">Name</option>
          <option value="price">Price (low to high)</option>
          <option value="-price">Price (high to low)</option>
        </select>
        <div class="relative">
          <input @input="onChangeSearch" type="text" class="text-sm pl-10 px-2 h-8 border border-gray-300 rounded-lg focus:outline-none focus:ring focus:border-blue ring-gray-200 transition" placeholder="Search">
          <img src="/search.svg" class="absolute top-2 left-3">
        </div>
        </div>
      </div>
      
      <CardList :items="items" />
    </div>
  </div>
</template>

<style scoped>
</style>
