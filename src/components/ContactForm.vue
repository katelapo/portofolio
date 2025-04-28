<script setup lang="ts">
import { ref } from 'vue';

const name = ref('m');
const email = ref('r');
const message = ref('h');
const isSending = ref(false);
const messageSent = ref(false);
const errorMessage = ref('');

const handleSubmit = async () => {
  isSending.value = true;
  errorMessage.value = '';

  // Simulasi pengiriman data (ganti dengan implementasi backend Anda)
  await new Promise(resolve => setTimeout(resolve, 2000));

  if (Math.random() > 0.8) {
    errorMessage.value = 'Terjadi kesalahan saat mengirim pesan. Silakan coba lagi nanti.';
  } else {
    messageSent.value = true;
    name.value = '';
    email.value = '';
    message.value = '';
  }

  isSending.value = false;
};
</script>

<template>
  <form @submit.prevent="handleSubmit" class="contact-form">
    <div v-if="messageSent" class="success-message">Pesan Anda telah terkirim!</div>
    <div v-if="errorMessage" class="error-message">{{ errorMessage }}</div>

    <div class="form-group">
      <label for="name">Nama:</label>
      <input type="text" id="name" v-model="name" required>
    </div>

    <div class="form-group">
      <label for="email">Email:</label>
      <input type="email" id="email" v-model="email" required>
    </div>

    <div class="form-group">
      <label for="message">Pesan:</label>
      <textarea id="message" v-model="message" rows="5" required></textarea>
    </div>

    <button type="submit" :disabled="isSending">
      <span v-if="isSending">Mengirim...</span>
      <span v-else>Kirim Pesan</span>
    </button>
  </form>
</template>

<style scoped>
.contact-form {
  max-width: 500px;
  margin: 0 auto;
  padding: 2rem;
  border: 1px solid #ddd;
  border-radius: 8px;
}

.form-group {
  margin-bottom: 1.5rem;
}

.form-group label {
  display: block;
  margin-bottom: 0.5rem;
  font-weight: bold;
}

.form-group input[type="text"],
.form-group input[type="email"],
.form-group textarea {
  width: 100%;
  padding: 0.75rem;
  border: 1px solid #ccc;
  border-radius: 4px;
  box-sizing: border-box;
}

.form-group textarea {
  resize: vertical;
}

.contact-form button {
  padding: 1rem 2rem;
  background-color: #007bff;
  color: white;
  border: none;
  border-radius: 5px;
  cursor: pointer;
  font-size: 1rem;
}

.contact-form button:disabled {
  background-color: #ccc;
  cursor: not-allowed;
}

.success-message {
  background-color: #d4edda;
  color: #155724;
  padding: 1rem;
  margin-bottom: 1rem;
  border-radius: 4px;
}

.error-message {
  background-color: #f8d7da;
  color: #721c24;
  padding: 1rem;
  margin-bottom: 1rem;
  border-radius: 4px;
}
</style>