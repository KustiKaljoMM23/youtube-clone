<template>
    <div class="column is-3">
      <div class="card video-item" @click="openRandom">
        <div class="card-image">
          <figure class="image is-16by9">
            <img :src="img" alt="Video" />
          </figure>
        </div>
        <div class="card-content has-background-dark has-text-white">
          <p class="title is-6">{{ title }}</p>
          <p class="subtitle is-7">{{ views }}</p>
        </div>
      </div>
    </div>
  </template>
  
  <script setup>
  const props = defineProps(['title', 'views', 'img'])
  
  const randomImages = [
    "https://placebear.com/400/200",
    "https://placebear.com/400/200",
    "https://placebeard.it/400x200",
    "https://baconmockup.com/400/200"
  ]
  
  function openRandom() {
    const random = randomImages[Math.floor(Math.random() * randomImages.length)];
    window.open(random, '_blank');
  }
  </script>
  
  <style scoped>
  .video-item {
    cursor: pointer;
  }
  
  .video-item:hover {
    transform: scale(1.05);
    transition: transform 0.2s;
  }
  </style>
  