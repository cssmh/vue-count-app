<script setup>
import { RouterLink, RouterView } from 'vue-router'
</script>

<template>
  <div class="app">
    <header>
      <nav>
        <RouterLink class="home" to="/">Home</RouterLink> |
        <RouterLink to="/about">About</RouterLink>
      </nav>
      <hr />
    </header>

    <RouterView />
  </div>
</template>

<style>
.app {
  font-family: Arial, sans-serif;
  text-align: center;
  padding: 20px;
}
</style>
