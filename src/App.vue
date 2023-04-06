<script setup lang="ts">
import {RouterView } from 'vue-router';
import navbar from './components/Frontend/navbar.vue';
</script>

<template>
  <header class="sticky top-0 z-30 w-full justify-center bg-opacity-90 backdrop-blur transition-all duration-100 bg-base-100 text-base-content shadow-sm">
    <nav class="navbar w-full">
      <navbar/>
    </nav>
  </header>

  <RouterView />
</template>


<style scoped>
</style>
