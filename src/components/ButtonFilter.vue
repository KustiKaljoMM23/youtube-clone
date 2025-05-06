<template>
  <div class="buttons are-small mb-4">
    <button 
      v-for="category in categories" 
      :key="category.name" 
      class="button is-rounded"
      :class="category.color"
      @click="$emit('filter', category.name)"
    >
      <span class="icon">{{ category.icon }}</span>
      <span>{{ category.name }}</span>
    </button>
  </div>
</template>

<script setup>
const categories = [
  { name: "All", icon: "🌐", color: "is-dark" },
  { name: "Music", icon: "🎵", color: "is-info" },
  { name: "Gaming", icon: "🎮", color: "is-danger" },
  { name: "Live", icon: "🔴", color: "is-success" },
  { name: "Comedy", icon: "😂", color: "is-warning" }
]
</script>
