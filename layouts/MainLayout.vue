<script setup lang="ts">
import AppHeader from "~/components/AppHeader.vue";
</script>
<template>
    <div class="hero-section-overlay"></div>
    <AppHeader />
    <slot />
    <AppFooter />
</template>

<style scoped lang="scss">
.hero-section-overlay {
    height: 100dvh;
    width: 100dvw;
    position: absolute;
    inset: 0;
    background: linear-gradient(-80deg, #346946, #417938, #5F7A57, #556A38, #395B58);
    background-size: 400% 400%;
    animation: gradient 25s ease infinite;
    z-index: -1;
}

@keyframes gradient {
    0% {
        background-position: 0% 50%;
    }

    50% {
        background-position: 100% 50%;
    }

    100% {
        background-position: 0% 50%;
    }
}
</style>