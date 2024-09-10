<script setup lang="ts">
import IconBackTrack from './icons/IconBackTrack.vue';
import IconLoop from './icons/IconLoop.vue';
import IconPlayTrack from './icons/IconPlayTrack.vue';
import IconQueueTrack from './icons/IconQueueTrack.vue';
</script>

<template>
    <div class="flex justify-evenly items-center gap-4 py-5">
        <i class="w-6 h-6 text-white/75 hover:text-white cursor-pointer transition duration-150 ease-in-out">
            <IconLoop />
        </i>
        <i class="w-6 h-6 text-white/75 hover:text-white cursor-pointer transition duration-150 ease-in-out">
            <IconBackTrack />
        </i>
        <i class="w-10 h-10 text-white/75 hover:text-white cursor-pointer transition duration-150 ease-in-out">
            <IconPlayTrack />
        </i>
        <i
            class="w-6 h-6 text-white/75 hover:text-white cursor-pointer transition duration-150 ease-in-out -rotate-180">
            <IconBackTrack />
        </i>
        <i class="w-6 h-6 text-white/75 hover:text-white cursor-pointer transition duration-150 ease-in-out">
            <IconQueueTrack />
        </i>
    </div>
</template>