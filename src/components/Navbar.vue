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
        <a class="navbar-item has-text-white">Sign In</a>
      </div>
    </div>
  </nav>

  <!-- Filter Buttons -->
  <ButtonFilter @filter="filterCategory" />
</template>

<script setup>
import ButtonFilter from './ButtonFilter.vue'

const emit = defineEmits(['filter'])

function filterCategory(category) {
  emit('filter', category)
}
</script>
