<script setup lang="ts">
import HeroSection from '@/components/HeroSection.vue';
import AboutMe from '@/components/AboutMe.vue';
import SkillsSection from '@/components/SkillsSection.vue';
import ProjectCard from '@/components/ProjectCard.vue';
import { ref } from 'vue';
import projectsData from '@/data/projects';

const featuredProjects = ref(projectsData.slice(0, 3)); // Tampilkan beberapa proyek unggulan
</script>

<template>
  <main>
    <HeroSection />
    <AboutMe />
    <SkillsSection />
    <section class="featured-projects">
      <h2>Proyek Unggulan</h2>
      <div class="projects-grid">
        <ProjectCard v-for="project in featuredProjects" :key="project.id" :project="project" />
      </div>
      <RouterLink to="/projects">Lihat Semua Proyek</RouterLink>
    </section>
  </main>
</template>

<style scoped>
.featured-projects {
  padding: 2rem;
  text-align: center;
}

.projects-grid {
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
  gap: 1.5rem;
  margin-bottom: 1rem;
}
</style>