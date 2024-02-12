<template>
    <div class="hero-section-overlay"></div>
    <main class="hero-section">
        <h1>Hi. I'm Piotr.<br>Frontend Developer</h1>
        <span class="hero-section-description">
            Building the bridges between design and technology, making the impossible, possible.
        </span>
    </main>
</template>

<style scoped lang="scss">
.hero-section {
    height: 100%;
    width: 100%;
    display: flex;
    flex-direction: column;
    justify-content: center;
    align-items: center;

    h1 {
        text-align: center;
        color: var(--color-lime-base);
        font-size: 72px;
        font-weight: 700;
    }
}

.hero-section-description {
    color: white;
    font-family: var(--font-base);
    font-size: 16px;
    margin-top: 60px;
    text-align: center;
}

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