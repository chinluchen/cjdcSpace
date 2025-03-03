<script setup>
import { RouterLink, RouterView } from 'vue-router'
import HelloWorld from './components/HelloWorld.vue'
</script>

<template>
  <header class="bg-gray-900 text-white py-5">
    <div class="container mx-auto flex flex-col items-center">
      <img alt="Vue logo" class="w-32 h-32 mb-4" src="@/assets/logo.svg" />

      <HelloWorld msg="You did it!" />

      <nav class="mt-4">
        <RouterLink to="/" class="px-4 py-2 text-lg hover:text-blue-400">Home</RouterLink>
        <RouterLink to="/about" class="px-4 py-2 text-lg hover:text-blue-400">About</RouterLink>
        <RouterLink to="/projects" class="px-4 py-2 text-lg hover:text-blue-400">Projects</RouterLink>
      </nav>
    </div>
  </header>

  <main class="min-h-screen flex items-center justify-center bg-gray-100">
    <RouterView />
  </main>
</template>

<style scoped>
nav a.router-link-exact-active {
  color: #38bdf8; /* Tailwind 的淺藍色 */
  font-weight: bold;
}

nav a.router-link-exact-active:hover {
  background-color: transparent;
}
</style>
