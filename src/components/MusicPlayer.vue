<script setup lang="ts">
import ButtonAction from './ButtonAction.vue';
import IconDotsMenu from './icons/IconDotsMenu.vue';
import IconMicrophone from './icons/IconMicrophone.vue';
import IconSpeaker from './icons/IconSpeaker.vue';
import IconSpeakerSound from './icons/IconSpeakerSound.vue';
import MusicPlayerActions from './MusicPlayerActions.vue';
import MusicPlayerHeader from './MusicPlayerHeader.vue';
</script>

<template>
    <div class="p-4 relative h-full flex flex-col">
        <div class="absolute inset-0 -z-10 bg-gradient-to-b from-black/75 to-black"></div>
        <video loop autoplay playsinline muted src="/BLANCO-MezzOra_Di_Sole.mp4"
            class="absolute inset-0 -z-20 object-cover object-center h-full w-full"></video>

        <!-- header -->
        <MusicPlayerHeader />

        <!-- Player -->
        <div class="grow flex flex-col items-center justify-center text-white">
            <h3 class="text-lg font-semibold py-5">
                In riproduzione
            </h3>

            <div class="px-10">
                <img src="https://i1.sndcdn.com/artworks-vat0q6c7SWYP-0-t500x500.jpg" alt="Copertina album Blanco"
                    title="Copertina album Blanco" />

                <div class="w-full flex items-center gap-2 py-5 px-2">
                    <div class="ml-auto flex flex-col justify-center items-center">
                        <h4 class="font-semibold">
                            Mezz'Ora di Sole
                        </h4>
                        <p class="font-semibold text-white/30">
                            BLANCO
                        </p>
                    </div>

                    <i
                        class="ml-auto text-white/50 hover:text-white transition duration-150 ease-in-out cursor-pointer">
                        <IconDotsMenu />
                    </i>
                </div>
            </div>

            <div class="grow px-10 w-full flex flex-col">
                <div class="flex gap-2 justify-center items-center">
                    <span class="font-semibold text-xs">
                        0:32
                    </span>
                    <div class="w-full h-1 rounded-2xl bg-white/50 overflow-hidden relative">
                        <div class="absolute left-0 top-0 bottom-0 w-2/12 bg-white rounded-2xl"></div>
                    </div>
                    <span class="font-semibold text-xs text-white/50">
                        1:58
                    </span>
                </div>


                <MusicPlayerActions class="grow" />

                <div class="flex gap-2 justify-between items-end">
                    <i
                        class="w-6 h-6 text-white/50 hover:text-white cursor-pointer transition duration-150 ease-in-out">
                        <IconSpeaker />
                    </i>

                    <ButtonAction>
                        <i>
                            <IconMicrophone />
                        </i>
                        Visualezzo testo
                    </ButtonAction>

                    <i
                        class="w-6 h-6 text-white/50 hover:text-white cursor-pointer transition duration-150 ease-in-out">
                        <IconSpeakerSound />
                    </i>
                </div>
            </div>

        </div>

    </div>
</template>