<script setup lang="ts">
import MusicPlayer from './components/MusicPlayer.vue';
import { RouterView } from 'vue-router'

</script>

<template>
  <div class="grid grid-cols-12 gap-2 bg-zinc-900 h-screen p-1.5">
    <main class="col-span-8 rounded-md overflow-hidden">
      <RouterView />
    </main>
    <aside class="bg-gray-100/10 backdrop-blur-xl col-span-4 rounded-md overflow-hidden">
      <MusicPlayer />
    </aside>
  </div>
</template>