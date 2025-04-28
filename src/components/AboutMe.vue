<script setup lang="ts">
const aboutText = `
  Ini adalah bagian tentang diri saya. Saya memiliki pengalaman dalam pengembangan web dengan fokus pada front-end dan back-end. Saya bersemangat tentang menciptakan solusi digital yang inovatif dan user-friendly.
  Saya memiliki keahlian dalam HTML, CSS, JavaScript, Vue.js, React, Node.js, dan banyak lagi. Saya selalu berusaha untuk belajar dan mengembangkan keterampilan saya.
`;
</script>

<template>
  <section class="about-me">
    <h2>Tentang Saya</h2>
    <p>{{ aboutText }}</p>
    </section>
</template>

<style scoped>
.about-me {
  padding: 2rem;
  text-align: center;
}

.about-me p {
  line-height: 1.6;
  margin-bottom: 1rem;
}
</style>