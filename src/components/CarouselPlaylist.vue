<script setup lang="ts">
import IconPlayTrack from './icons/IconPlayTrack.vue';
</script>

<template>
    <div class="w-full pt-20 pb-10 bg-gradient-to-r from-teal-500 to-red-700">
        <div class="flex justify-center items-center overflow-x-hidden w-full gap-20 pt-20 pb-10">
            <div
                class="bg-gradient-to-r from-teal-400 to-red-600 rounded-2xl relative min-w-[500px] max-w-lg w-full h-48">
                <img class="absolute bottom-0 left-4 h-full w-auto scale-125 -translate-y-6"
                    src="/public/spotify-fresh-finds-no-bg.png" alt="Immagine di copertina fresh finds" />
                <div class="text-white absolute top-1/2 left-1/2 -translate-y-1/2 flex gap-1">
                    <i class="w-10 h-10">
                        <IconPlayTrack />
                    </i>
                    <div>
                        <h2 class="font-semibold uppercase text-lg leading-none">Wallice</h2>
                        <h3 class="font-bold uppercase text-2xl leading-none">Fresh finds</h3>
                    </div>
                </div>
            </div>
            <div
                class="bg-gradient-to-r from-teal-400 to-red-600 rounded-2xl relative min-w-[500px] max-w-md w-full h-48 scale-125">
                <img class="absolute bottom-0 left-5 h-full w-auto scale-125 -translate-y-6"
                    src="/public/spotify-fresh-finds-no-bg.png" alt="Immagine di copertina fresh finds" />
                <div class="text-white absolute top-1/2 left-1/2 -translate-y-1/2 flex gap-1">
                    <i class="w-10 h-10">
                        <IconPlayTrack />
                    </i>
                    <div>
                        <h2 class="font-semibold uppercase text-lg leading-none">Wallice</h2>
                        <h3 class="font-bold uppercase text-2xl leading-none">Fresh finds</h3>
                    </div>
                </div>
            </div>
            <div
                class="bg-gradient-to-r from-teal-400 to-red-600 rounded-2xl relative min-w-[500px] max-w-md w-full h-48">
                <img class="absolute bottom-0 left-4 h-full w-auto scale-125 -translate-y-6"
                    src="/public/spotify-fresh-finds-no-bg.png" alt="Immagine di copertina fresh finds" />
                <div class="text-white absolute top-1/2 left-1/2 -translate-y-1/2 flex gap-1">
                    <i class="w-10 h-10">
                        <IconPlayTrack />
                    </i>
                    <div>
                        <h2 class="font-semibold uppercase text-lg leading-none">Wallice</h2>
                        <h3 class="font-bold uppercase text-2xl leading-none">Fresh finds</h3>
                    </div>
                </div>
            </div>
        </div>
    </div>
</template>