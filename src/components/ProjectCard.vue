<script setup lang="ts">
import { defineProps } from 'vue';

interface Project {
  id: number;
  title: string;
  description: string;
  image: string;
  link?: string;
}

defineProps<{
  project: Project;
}>();
</script>

<template>
  <div class="project-card">
    <img :src="project.image" :alt="project.title">
    <h3>{{ project.title }}</h3>
    <p>{{ project.description }}</p>
    <a v-if="project.link" :href="project.link" target="_blank">Lihat Proyek</a>
  </div>
</template>

<style scoped>
.project-card {
  border: 1px solid #ddd;
  border-radius: 8px;
  overflow: hidden;
  box-shadow: 0 2px 4px rgba(0, 0, 0, 0.1);
}

.project-card img {
  width: 100%;
  display: block;
  height: auto;
}

.project-card h3 {
  padding: 1rem;
  margin: 0;
  font-size: 1.2rem;
}

.project-card p {
  padding: 0 1rem 1rem;
  margin: 0;
  line-height: 1.5;
}

.project-card a {
  display: block;
  padding: 1rem;
  background-color: #007bff;
  color: white;
  text-align: center;
  text-decoration: none;
}

.project-card a:hover {
  background-color: #0056b3;
}
</style>