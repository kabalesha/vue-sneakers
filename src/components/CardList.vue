<script setup>
import Card from './Card.vue'

const onClickAdd = () => {
  alert('Add')
}
</script>
<template>
  <div class="grid grid-cols-4 gap-5">
    <Card
      imageUrl="/sneakers/sneakers-1.jpg"
      title="Sneakers"
      :price="5000"
      :isAdded="true"
      :isFavorite="true"
      :onClickAdd="onClickAdd"
    />
    <Card imageUrl="/sneakers/sneakers-2.jpg" title="Sneakers" :price="5000" />
    <Card imageUrl="/sneakers/sneakers-3.jpg" title="Sneakers" :price="5000" />
    <Card imageUrl="/sneakers/sneakers-4.jpg" title="Sneakers" :price="5000" />
    <Card imageUrl="/sneakers/sneakers-5.jpg" title="Sneakers" :price="5000" />
    <Card imageUrl="/sneakers/sneakers-6.jpg" title="Sneakers" :price="5000" />
    <Card imageUrl="/sneakers/sneakers-7.jpg" title="Sneakers" :price="5000" />
    <Card imageUrl="/sneakers/sneakers-8.jpg" title="Sneakers" :price="5000" />
    <Card imageUrl="/sneakers/sneakers-9.jpg" title="Sneakers" :price="5000" />
    <Card imageUrl="/sneakers/sneakers-10.jpg" title="Sneakers" :price="5000" />
    <Card imageUrl="/sneakers/sneakers-11.jpg" title="Sneakers" :price="5000" />
    <Card imageUrl="/sneakers/sneakers-12.jpg" title="Sneakers" :price="5000" />
  </div>
</template>
