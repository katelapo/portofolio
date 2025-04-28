<script setup lang="ts">
import { ref } from 'vue';
import skillsData from '@/data/skills';

const skills = ref(skillsData);
</script>

<template>
  <section class="skills">
    <h2>Keahlian</h2>
    <ul class="skills-list">
      <li v-for="skill in skills" :key="skill.name">
        {{ skill.name }} <span v-if="skill.level">({{ skill.level }})</span>
      </li>
    </ul>
  </section>
</template>

<style scoped>
.skills {
  padding: 2rem;
  text-align: center;
}

.skills-list {
  list-style: none;
  padding: 0;
  margin: 0;
  display: flex;
  flex-wrap: wrap;
  justify-content: center;
}

.skills-list li {
  background-color: #eee;
  padding: 0.5rem 1rem;
  margin: 0.5rem;
  border-radius: 5px;
}
</style>