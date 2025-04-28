<script setup lang="ts">
import { RouterView } from 'vue-router';
import Navbar from '@/components/Navbar.vue';

// Anda bisa menambahkan state atau logika global di sini jika diperlukan
</script>

<template>
  <div class="app-container">
    <Navbar />
    <RouterView />
  </div>
</template>

<style scoped>
.app-container {
  font-family: 'Arial', sans-serif; /* Contoh font */
  display: flex;
  flex-direction: column;
  min-height: 100vh;
}
</style>