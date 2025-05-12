<template>
  <nav class="navbar has-background-black">
    <div class="navbar-brand">
      <a class="navbar-item has-text-white">
        <strong>YouTube</strong>
      </a>
    </div>

    <div class="navbar-menu">
      <div class="navbar-start">
        <div class="navbar-item">
          <input class="input" type="search" placeholder="Search" />
        </div>
      </div>
      <div class="navbar-end">
        <!-- Sign In Button -->
        <a class="navbar-item has-text-white" @click="showSignIn = !showSignIn" style="cursor: pointer;">Sign In</a>
      </div>
    </div>
  </nav>

  <!-- Filter Buttons -->
  <ButtonFilter @filter="filterCategory" />

  <!-- Sign In Form -->
  <div v-if="showSignIn" style="position: absolute; top: 60px; right: 20px; z-index: 1000;">
    <SignInForm />
  </div>
</template>

<script setup>
import { ref } from 'vue'
import ButtonFilter from './ButtonFilter.vue'
import SignInForm from './SignInForm.vue'

const emit = defineEmits(['filter'])
const showSignIn = ref(false)

function filterCategory(category) {
  emit('filter', category)
}
</script>
