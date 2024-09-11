<script setup lang="ts">
import IconChevronFilled from '@/components/icons/IconChevronFilled.vue';
import IconSearch from '@/components/icons/IconSearch.vue';
</script>

<template>
    <header class="flex gap-4 justify-between items-center p-4 absolute top-0 w-full">
        <ul class="flex justify-center items-center gap-6 text-white/50 text-sm">
            <li class="hover:text-white transistion duration-150 ease-in-out">
                <RouterLink to="/">
                    Home
                </RouterLink>
            </li>
            <li class="hover:text-white transistion duration-150 ease-in-out">
                <RouterLink to="/">
                    Esplora
                </RouterLink>
            </li>
            <li class="hover:text-white transistion duration-150 ease-in-out">
                <RouterLink to="/">
                    Playlist
                </RouterLink>
            </li>
        </ul>

        <label for="search"
            class="bg-black/10 rounded-full max-w-sm w-full px-5 py-2 text-center text-white flex items-center gap-1">
            <i>
                <IconSearch />
            </i>
            <input type="text" name="search" id="search" placeholder="Cerca"
                class="bg-transparent border-none outline-none w-full">
        </label>

        <button type="button"
            class="p-1 bg-black/20 backdrop-blur-md rounded-full flex gap-1 justify-center items-center">
            <img class="w-7 h-7 aspect-square rounded-full" src="/public/profile-black.png" alt="Immagine progilo">
            <i class="text-white w-5 h-5 pr-1">
                <IconChevronFilled />
            </i>
        </button>
    </header>
</template>