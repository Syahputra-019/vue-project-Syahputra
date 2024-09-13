<script setup lang="ts">
import { RouterLink, RouterView } from 'vue-router'
import ClickCounter from './components/ClickCounter.vue'
import BoxColorChanger from './components/BoxColorChanger.vue'
import ImageCarousel from './components/ImageCarousel.vue'
</script>

<template>
  <div id="app">
    <header>
      <img alt="Vue logo" class="logo" src="@/assets/logo.svg" width="125" height="125" />
      <div class="wrapper">
        <nav>
          <RouterLink to="/">Home</RouterLink>
          <RouterLink to="/about">About</RouterLink>
        </nav>
      </div>
    </header>

    <main>
      <ClickCounter />
      <BoxColorChanger />
      <ImageCarousel />
    </main>
    
    <RouterView />
  </div>
</template>

<style scoped>
/* Header Styles */
header {
  background-color: #00796b;
  padding: 20px;
  text-align: center;
  color: white;
  line-height: 1.5;
  max-height: 100vh;
}

.logo {
  display: block;
  margin: 0 auto 1rem;
  border-radius: 50%; /* Circular logo */
  box-shadow: 0 4px 8px rgba(0, 0, 0, 0.1); /* Add shadow */
}

nav {
  width: 100%;
  font-size: 16px;
  margin-top: 1.5rem;
}

nav a {
  color: white;
  text-decoration: none;
  padding: 10px 15px;
  margin: 0 5px;
  border-radius: 5px;
  transition: background-color 0.3s;
}

nav a.router-link-exact-active {
  background-color: #004d40;
}

nav a:hover {
  background-color: rgba(255, 255, 255, 0.2);
}

main {
  display: flex;
  flex-direction: column;
  align-items: center;
  padding: 40px;
  background-color: #e0f7fa;
  border-radius: 10px;
  box-shadow: 0 4px 12px rgba(0, 0, 0, 0.1);
  margin: 30px;
}

/* Responsive layout for larger screens */
@media (min-width: 1024px) {
  header {
    display: flex;
    justify-content: space-between;
    align-items: center;
    padding: 20px 50px;
  }

  .logo {
    margin: 0 20px 0 0;
  }

  nav {
    margin-top: 0;
  }

  main {
    padding: 50px;
    width: 80%;
    max-width: 1200px;
  }
}
</style>
