<template>
  <div class="click-counter">
    <h2>Click Counter</h2>
    <button @click="incrementCount">Click Me!</button>
    <p>You have clicked the button {{ count }} times.</p>
  </div>
</template>

<script setup lang="ts">
import { ref } from 'vue'

const count = ref(0)

function incrementCount() {
  count.value++
}
</script>

<style scoped>
.click-counter {
  text-align: center;
  margin: 20px;
}

button {
  padding: 10px 20px;
  font-size: 16px;
  cursor: pointer;
}
</style>
