<script setup lang="ts">
import { ref } from 'vue';

import IconsPodCast from '@/components/icons/IconsPodCast.vue';
import IconAlbum from '@/components/icons/IconAlbum.vue';
import IconArtist from '@/components/icons/IconArtist.vue';

const recentListens = ref<{ type: string, title: string, desc?: string, imageUrl: string }[]>([
    {
        type: 'PodCast',
        title: 'La libreria tascabile',
        desc: 'Episodio 23: Sangue amaro',
        imageUrl: 'libreria-tascabile.jpg'
    },
    {
        type: 'Artista',
        title: 'DitoNellaPiaga',
        imageUrl: 'ditonellapiaga.jpg'
    },
    {
        type: 'Artista',
        title: 'MACE',
        imageUrl: 'mace-profile.jpg'
    },
    {
        type: 'Album',
        title: 'MACE',
        desc: 'OBE',
        imageUrl: 'mace-obe.png'
    },
    {
        type: 'Album',
        title: 'Fall Out Boy',
        desc: 'Save Rock & Roll',
        imageUrl: 'fallout-boy.jpg'
    },
    {
        type: 'Album',
        title: 'Twenty One Pilots',
        desc: 'Blurryface',
        imageUrl: 'twenty-one-pilots.jpg'
    },
]);
</script>

<template>
    <div class="mb-8">
        <h3 class="font-semibold mb-4">
            Ascoltati di recente
        </h3>

        <div class="flex flex-nowrap gap-10 justify-start items-start overflow-x-auto">
            <template v-for="(element, i) in recentListens" :key="i">
                <div
                    class="grow cursor-pointer flex flex-col justify-center items-center min-w-36 w-full max-w-36 p-1 rounded-lg overflow-hidden">
                    <img :class="element.type.toLowerCase().includes('artista') ? 'rounded-full' : ''"
                        class="grow h-full w-full aspect-square object-cover object-center block"
                        :src="element.imageUrl" :alt="'Copertina ' + element.title">
                    <div class="grow text-center py-2">
                        <span class="mb-2 text-sm text-white/50 flex justify-center items-center gap-2">
                            <i>
                                <IconsPodCast v-if="element.type.toLowerCase().includes('podcast')" />
                                <IconAlbum v-if="element.type.toLowerCase().includes('album')" />
                                <IconArtist v-if="element.type.toLowerCase().includes('artista')" />
                            </i>
                            {{ element.type }}
                        </span>
                        <p class="text-xs text-white/75 font-semibold px-1">{{ element.title }}</p>
                        <p class="font-semibold leading-none px-1">{{ element.desc }}</p>
                    </div>
                </div>
            </template>
        </div>
    </div>
</template>