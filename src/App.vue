<script setup>
import { onMounted, ref } from 'vue'
import axios from 'axios'
import Header from './components/Header/Header.vue'
import CardList from './components/CardList.vue'
import Drawer from './components/Drawer.vue'

const items = ref([])
onMounted(async () => {
  try {
    const { data } = await axios.get('https://78e26eecca6020b8.mokky.dev/items')
    items.value = data
  } catch (error) {
    console.log(error)
  }
})
</script>

<template>
  <div class="bg-white w-4/5 m-auto rounded-xl shadow-xl mt-14">
    <!-- <Drawer /> -->
    <Header />
    <div class="p-10">
      <div class="flex justify-between items-center">
        <h2 class="text-3xl font-bold mb-8">All staff</h2>

        <div class="flex gap-4">
          <select class="py-2 px-3 border rounded-md outline-none">
            <option value="">By name</option>
            <option value="">From low to high price</option>
            <option value="">From high to low price</option>
          </select>

          <div class="relative">
            <img src="/search.svg" class="absolute left-4 top-3" alt="" />
            <input
              class="border rounded-md py-2 pl-11 pr-4 outline-none focus:border-gray-400"
              type="text"
              placeholder="Search..."
            />
          </div>
        </div>
      </div>
      <div class="mt-10">
        <CardList :items="items" />
      </div>
    </div>
  </div>
</template>
