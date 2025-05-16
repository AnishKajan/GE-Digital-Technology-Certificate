<template>
  <div class="container">
    <h1>Compute Product</h1>
    <img src="https://images.unsplash.com/photo-1504198266285-165d2de8ab2d" alt="Airplane wing" class="image" />
    
    <p>Number 1: {{ num1 }}</p>
    <p>Number 2: {{ num2 }}</p>

    <button v-if="!computed" @click="computeProduct">Compute</button>

    <p v-else>Product: {{ product }}</p>
  </div>
</template>

<script setup>
import { ref } from 'vue'

const num1 = ref(7)
const num2 = ref(3)
const product = ref(0)
const computed = ref(false)

function computeProduct() {
  product.value = num1.value * num2.value
  computed.value = true
}
</script>

<style scoped>
.container {
  font-family: Arial, sans-serif;
  text-align: center;
  margin-top: 40px;
}
.image {
  width: 300px;
  margin: 20px auto;
  display: block;
}
button {
  margin-top: 20px;
  padding: 10px 20px;
  font-size: 16px;
}
</style>
