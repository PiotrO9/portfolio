<template>
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
        font-weight: 700;
        font-size: 60px;

        @media (width > 1024px) {
            font-size: 90px;
        }

        @media (width > 1024px) {
            font-size: 120px;
        }
    }
}

.hero-section-description {
    color: white;
    font-family: var(--font-base);
    font-size: 16px;
    margin-top: 60px;
    text-align: center;
    max-width: 90vw;

    @media (width > 1024px) {
        font-size: 24px;
    }

    @media (width > 1600px) {
        font-size: 28px;
    }
}
</style>