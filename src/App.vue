<script setup>
import Header from './components/Header/Header.vue'
import CardList from './components/CardList.vue'
import Drawer from './components/Drawer.vue'
</script>

<template>
  <div class="bg-white w-4/5 m-auto rounded-xl shadow-xl mt-14">
    <Drawer />
    <Header />

    <div class="p-10">
      <h2 class="text-3xl font-bold mb-10">All staff</h2>
      <CardList />
    </div>
  </div>
</template>
