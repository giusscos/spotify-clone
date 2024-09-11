<script setup lang="ts">
import NavHeader from '@/components/NavHeader.vue';
import CarouselPlaylist from '@/components/CarouselPlaylist.vue';
import RecentListens from '@/components/RecentListens.vue';
import SuggestedPlaylist from '@/components/SuggestedPlaylist.vue';
</script>

<template>
  <div class="relative flex flex-col h-full overflow-auto">
    <NavHeader />

    <CarouselPlaylist />
    <div class="bg-black text-white p-5 w-full grow">

      <RecentListens />

      <SuggestedPlaylist />
    </div>
  </div>
</template>