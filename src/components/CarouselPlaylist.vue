<script setup lang="ts">
import { onMounted, ref } from 'vue';
import IconPlayTrack from './icons/IconPlayTrack.vue';

const currentImageIndex = ref<number>(0);
const carouselItems = ref<any>([]);

const contents = ref<{ title: string, subTitle?: string, imageUrl: string }[]>([
    {
        title: 'Weelice',
        subTitle: 'Fresh finds',
        imageUrl: '/public/spotify-fresh-finds-no-bg.png'
    },
    {
        title: 'Weelice',
        subTitle: 'Fresh finds',
        imageUrl: '/public/spotify-fresh-finds-no-bg.png'
    },
    {
        title: 'Weelice',
        subTitle: 'Fresh finds',
        imageUrl: '/public/spotify-fresh-finds-no-bg.png'
    },
])

function observeImages() {
    const options = {
        root: null, // Usa il viewport come radice per il calcolo
        rootMargin: '0px',
        threshold: 0.5, // Trigger quando il 50% dell'immagine è visibile
    };

    const observer = new IntersectionObserver((entries) => {
        entries.forEach((entry) => {
            if (entry.isIntersecting) {
                const index = carouselItems.value.indexOf(entry.target);
                currentImageIndex.value = index;
            }
        });
    }, options);

    carouselItems.value.forEach((item: any) => {
        observer.observe(item);
    });
};

onMounted(() => {
    carouselItems.value = Array.from(document.querySelectorAll('.carousel-item'));
    observeImages();
});
</script>

<template>
    <div class="w-full pt-20 pb-10 bg-gradient-to-r from-teal-500 to-red-700">
        <div class="flex items-center overflow-x-auto w-full gap-40 pt-20 pb-10 px-40 snap-x"
            style="scrollbar-width: none;">
            <template v-for="(element, index) in contents" :key="'carousel ' + index">
                <div ref="carouselItems" :class="{
                    'scale-125': currentImageIndex === index,
                    'scale-90': currentImageIndex !== index,
                }"
                    class="carousel-item snap-center snap-normal bg-gradient-to-r from-teal-400 to-red-600 rounded-2xl relative min-w-[500px] max-w-lg w-full h-48 transition duration-150 ease-in-out">
                    <img class="absolute bottom-0 left-4 h-full w-auto scale-125 -translate-y-6" :src="element.imageUrl"
                        :alt="'Copertina ' + element.title" />
                    <div class="text-white absolute top-1/2 left-1/2 -translate-y-1/2 flex gap-1">
                        <i class="w-10 h-10">
                            <IconPlayTrack />
                        </i>
                        <div>
                            <h2 class="font-semibold uppercase text-lg leading-none">{{ element.title }}</h2>
                            <h3 class="font-bold uppercase text-2xl leading-none">{{ element.subTitle }}</h3>
                        </div>
                    </div>
                </div>
            </template>
        </div>
    </div>
</template>