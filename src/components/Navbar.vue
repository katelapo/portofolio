<script setup lang="ts">
import { RouterLink } from 'vue-router';


// Anda bisa menambahkan logika untuk menu responsif di sini
</script>

<template>
  <nav>
    <div class="logo">Portofolio Anda</div>
    <ul>
      <li><RouterLink to="/">Beranda</RouterLink></li>
      <li><RouterLink to="/project">Proyek</RouterLink></li>
      <li><RouterLink to="/contact">Kontak</RouterLink></li>
      <li><a href="/cv.pdf" target="_blank">CV</a></li>
    </ul>
  </nav>
</template>

<style scoped>
nav {
  background-color: #333;
  color: white;
  padding: 1rem 2rem;
  display: flex;
  justify-content: space-between;
  align-items: center;
}

nav ul {
  list-style: none;
  padding: 0;
  margin: 0;
  display: flex;
}

nav li {
  margin-left: 1.5rem;
}

nav a {
  color: white;
  text-decoration: none;
}

.logo {
  font-size: 1.5rem;
  font-weight: bold;
}
</style>