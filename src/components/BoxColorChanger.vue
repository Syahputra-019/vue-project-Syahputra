<template>
  <div class="box-color-changer">
    <h2>Box Color Changer</h2>
    <button @click="changeColor">Change Color</button>
    <div class="color-box" :style="{ backgroundColor: color }"></div>
  </div>
</template>

<script setup lang="ts">
import { ref } from 'vue'

const colors = ['#FF6347', '#4CAF50', '#1E90FF', '#FFD700', '#FF69B4']
const color = ref(colors[0])

function changeColor() {
  color.value = colors[Math.floor(Math.random() * colors.length)]
}
</script>

<style scoped>
.box-color-changer {
  text-align: center;
  margin: 20px;
}

button {
  padding: 10px 20px;
  font-size: 16px;
  cursor: pointer;
}

.color-box {
  width: 100px;
  height: 100px;
  margin: 20px auto;
  border: 1px solid #000;
}
</style>
