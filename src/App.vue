<template>
  <div class="columns is-gapless has-background-dark has-text-white">
    <Sidebar />
    <main class="column p-5">
      <Navbar />
      <VideoGrid />
    </main>
  </div>
</template>

<script setup>
import Navbar from './components/Navbar.vue'
import Sidebar from './components/Sidebar.vue'
import VideoGrid from './components/VideoGrid.vue'
</script>

<style>
body {
  margin: 0;
}
</style>
