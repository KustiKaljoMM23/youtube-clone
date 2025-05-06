<template>
  <div class="columns is-multiline" id="video-grid">
    <VideoItem
      v-for="(video, index) in filteredVideos"
      :key="index"
      :title="video.title"
      :views="video.views"
      :img="video.img"
    />
  </div>
</template>

<script setup>
import { computed } from 'vue'
import VideoItem from './VideoItem.vue'

const props = defineProps(['category'])
  
  const videos = [
    // Row 1
    { title: "Funny Bear Video", views: "1M views • 1 day ago", img: "https://placebear.com/200/301" },
    { title: "Bear Adventures", views: "500K views • 2 days ago", img: "https://placebear.com/320/180" },
    { title: "Another Bear Video", views: "300K views • 5 days ago", img: "https://placebear.com/352/180" },
    { title: "Bear Comedy", views: "200K views • 1 week ago", img: "https://placebear.com/321/180" },
    
    // Row 2
    { title: "Tech Reviews", views: "800K views • 3 days ago", img: "https://placebear.com/331/180" },
    { title: "Travel Vlog", views: "2M views • 1 week ago", img: "https://placebear.com/322/180" },
    { title: "Cooking Show", views: "900K views • 2 weeks ago", img: "https://placebear.com/125/180" },
    { title: "Gaming Highlights", views: "1.2M views • 5 days ago", img: "https://placebear.com/323/180" },
    
    // Row 3
    { title: "DIY Crafts", views: "700K views • 4 days ago", img: "https://placebear.com/421/180" },
    { title: "Movie Trailers", views: "5M views • 2 days ago", img: "https://placebear.com/324/180" },
    { title: "Workout Routine", views: "600K views • 1 week ago", img: "https://placebear.com/351/180" },
    { title: "Art Time-lapse", views: "850K views • 3 days ago", img: "https://placebear.com/523/180" }
  ]
  const filteredVideos = computed(() => {
  if (props.category === 'All') return videos
  return videos.filter(v => v.category === props.category)
})
</script>
  