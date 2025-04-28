<script setup lang="ts">
import ProjectCard from '@/components/ProjectCard.vue';
import { ref } from 'vue';
import projectsData from '@/data/projects';

const projects = ref(projectsData);
</script>

<template>
  <main class="projects-view">
    <h2>Semua Proyek</h2>
    <div class="projects-grid">
      <ProjectCard v-for="project in projects" :key="project.id" :project="project" />
    </div>
  </main>
</template>

<style scoped>
.projects-view {
  padding: 2rem;
  text-align: center;
}

.projects-grid {
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
  gap: 1.5rem;
  margin-top: 1rem;
}
</style>