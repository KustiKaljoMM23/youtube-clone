<template>
  <div class="columns is-gapless has-background-dark has-text-white">
    <Sidebar />
    <main class="column p-5">
      <Navbar @filter="currentCategory = $event" />
      <VideoGrid :category="currentCategory" />
    </main>
  </div>
</template>

<script setup>
import { ref } from 'vue'
import Navbar from './components/Navbar.vue'
import Sidebar from './components/Sidebar.vue'
import VideoGrid from './components/Videogrid.vue'

const currentCategory = ref('All')
</script>

<style>
body {
  margin: 0;
}
</style>
