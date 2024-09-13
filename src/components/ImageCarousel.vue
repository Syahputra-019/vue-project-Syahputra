<template>
  <div class="image-carousel">
    <h2>Image Carousel</h2>
    <button @click="prevImage">Previous</button>
    <img :src="images[currentIndex]" alt="carousel image" class="carousel-image" />
    <button @click="nextImage">Next</button>
  </div>
</template>

<script setup lang="ts">
import { ref } from 'vue'

const images = [
  'https://via.placeholder.com/150/FF6347/FFFFFF?text=Image+1',
  'https://via.placeholder.com/150/4CAF50/FFFFFF?text=Image+2',
  'https://via.placeholder.com/150/1E90FF/FFFFFF?text=Image+3'
]
const currentIndex = ref(0)

function prevImage() {
  currentIndex.value = (currentIndex.value - 1 + images.length) % images.length
}

function nextImage() {
  currentIndex.value = (currentIndex.value + 1) % images.length
}
</script>

<style scoped>
.image-carousel {
  text-align: center;
  margin: 20px;
}

.carousel-image {
  width: 150px;
  height: 150px;
  display: block;
  margin: 0 auto;
}

button {
  padding: 10px 20px;
  font-size: 16px;
  cursor: pointer;
}
</style>
