<template>
  <div style="background: #222; padding: 1rem; border-radius: 8px; color: white; width: 300px;">
    <h2>Sign In</h2>
    <form @submit.prevent="handleSubmit">
      <div style="margin-bottom: 0.5rem;">
        <label>Name:</label>
        <input v-model="name" type="text" required />
      </div>
      <div style="margin-bottom: 0.5rem;">
        <label>Email:</label>
        <input v-model="email" type="email" required />
      </div>
      <div style="margin-bottom: 0.5rem;">
        <label>Password:</label>
        <input v-model="password" type="password" required />
      </div>
      <button type="submit">Submit</button>
    </form>
  </div>
</template>

<script setup>
import { ref } from 'vue'

const name = ref('')
const email = ref('')
const password = ref('')

function handleSubmit() {
  alert(`Name: ${name.value}\nEmail: ${email.value}\nPassword: ${password.value}`)
}
</script>

<style scoped>
input {
  width: 100%;
  padding: 0.3rem;
  margin-top: 0.2rem;
}
button {
  margin-top: 0.5rem;
  padding: 0.4rem 1rem;
  cursor: pointer;
}
</style>
