<script setup lang="ts">
import { ref } from 'vue';

const suggestedPlaylist = ref<{ imageUrl: string }[]>([
    {
        imageUrl: 'libreria-tascabile.jpg'
    },
    {
        imageUrl: 'ditonellapiaga.jpg'
    },
    {
        imageUrl: 'fallout-boy.jpg'
    },
    {
        imageUrl: 'twenty-one-pilots.jpg'
    }
]);
</script>
<template>
    <div>
        <h3 class="font-semibold mb-4">
            Playlist consigliate
        </h3>

        <div class="flex flex-nowrap gap-10 justify-start items-start overflow-x-auto">
            <template v-for="(element, i) in suggestedPlaylist" :key="i">
                <div
                    class="grow cursor-pointer flex flex-col justify-center items-center min-w-64 w-full max-w-64 rounded-lg overflow-hidden">
                    <img class="grow h-full w-full aspect-video object-cover object-center block"
                        :src="element.imageUrl" :alt="'Copertina' + i">
                </div>
            </template>
        </div>
    </div>
</template>