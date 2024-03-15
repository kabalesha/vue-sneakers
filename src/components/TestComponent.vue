<script setup>
defineProps({
  title: String,
  price: String
})
</script>
<template>
  <div class="product">
    <h1>Product: {{ title }}</h1>
    <h2>Price: {{ price }}</h2>
  </div>
</template>
<style scoped>
.product {
  border: 1px solid black;
  padding: 10px;
  margin-bottom: 10px;
}
</style>
