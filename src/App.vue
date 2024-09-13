<script setup lang="ts">
import { RouterLink, RouterView } from 'vue-router'
import HelloWorld from './components/HelloWorld.vue'
</script>

<template>
  <header>
    <img alt="Vue logo" class="logo" src="@/assets/logo.svg" width="125" height="125" />

    <div class="wrapper">
      <HelloWorld msg="You did it!" />

      <nav>
        <RouterLink to="/">Home</RouterLink>
        <RouterLink to="/about">About</RouterLink>
      </nav>
    </div>
  </header>

  <RouterView />
</template>

<style scoped>
header {
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: center;
  height: 100vh;
  background: linear-gradient(135deg, #4facfe 0%, #00f2fe 100%);
  color: #fff;
  transition: all 0.3s ease;
}

.logo {
  display: block;
  margin: 0 auto 2rem;
  transition: transform 0.3s ease;
}

.logo:hover {
  transform: rotate(360deg);
}

nav {
  width: 100%;
  font-size: 1.2rem;
  text-align: center;
  margin-top: 2rem;
  transition: color 0.3s ease, background-color 0.3s ease;
}

nav a {
  display: inline-block;
  padding: 0.5rem 1.5rem;
  margin: 0 0.5rem;
  text-decoration: none;
  color: #fff;
  border: 2px solid transparent;
  border-radius: 25px;
  transition: all 0.3s ease;
}

nav a.router-link-exact-active {
  background-color: rgba(255, 255, 255, 0.2);
  border-color: #fff;
}

nav a:hover {
  background-color: #fff;
  color: #00f2fe;
}

@media (min-width: 1024px) {
  header {
    flex-direction: row;
    justify-content: space-between;
    padding: 2rem;
  }

  .logo {
    margin: 0;
  }

  header .wrapper {
    display: flex;
    flex-direction: column;
    align-items: flex-start;
  }

  nav {
    text-align: left;
    margin: 0;
    font-size: 1.2rem;
  }

  nav a {
    padding: 0.5rem 2rem;
  }
}
</style>
