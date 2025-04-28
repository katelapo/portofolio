<script setup lang="ts">
import ContactForm from '@/components/ContactForm.vue';
</script>

<template>
  <main class="contact-view">
    <h2>Hubungi Saya</h2>
    <p>Silakan isi formulir di bawah ini untuk menghubungi saya.</p>
    <ContactForm />
  </main>
</template>

<style scoped>
.contact-view {
  padding: 2rem;
  text-align: center;
}
</style>