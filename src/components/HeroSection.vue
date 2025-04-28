<script setup lang="ts">
const name = 'Muhammad Ramadani Hubillah';
const tagline = 'Mahasiswa Teknik Informatika';
const description = 'Universitas Yudharta Pasuruan';
</script>

<template>
  <section class="hero">
    <h1>Halo, Saya {{ name }}</h1>
    <p class="tagline">{{ tagline }}</p>
    <p class="description">{{ description }}</p>
    <button>Hubungi Saya</button>
  </section>
</template>

<style scoped>
.hero {
  background-color: #f0f0f0;
  padding: 4rem 2rem;
  text-align: center;
}

.hero h1 {
  font-size: 2.5rem;
  margin-bottom: 0.5rem;
}

.hero .tagline {
  font-size: 1.2rem;
  color: #777;
  margin-bottom: 1rem;
}

.hero .description {
  line-height: 1.6;
  margin-bottom: 2rem;
}

.hero button {
  padding: 1rem 2rem;
  background-color: #007bff;
  color: white;
  border: none;
  border-radius: 5px;
  cursor: pointer;
  font-size: 1rem;
}
</style>