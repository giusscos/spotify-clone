<script setup lang="ts">
import ButtonAction from './ButtonAction.vue';
import IconRadar from './icons/IconRadar.vue';
import IconResize from './icons/IconResize.vue';
import IconShare from './icons/IconShare.vue';
</script>

<template>
    <div class="flex justify-between items-center">
        <ButtonAction>
            <i class="text-green-500">
                <IconRadar />
            </i>
            Discover
        </ButtonAction>
        <div class="flex gap-4 items-center justify-center">
            <ButtonAction>
                <i>
                    <IconShare />
                </i>
            </ButtonAction>
            <ButtonAction>
                <i class="-rotate-45">
                    <IconResize />
                </i>
            </ButtonAction>
        </div>
    </div>
</template>