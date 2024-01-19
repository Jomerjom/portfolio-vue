<script setup>

defineProps({
    miniPitch: String,
    yourName: String,
    imagePath: String,
})

const scrollToSection = (event, id) => {
    event.preventDefault();
    const element = document.getElementById(id);

    if (element) {
        const targetPosition =
            element.getBoundingClientRect().top +
            window.scrollY -
            window.innerHeight / 2 +
            element.getBoundingClientRect().height / 2;

        window.scrollTo({
            top: targetPosition,
            behavior: "smooth",
        });
    }
};

</script>

<template>
    <section class="hero">
        <div class="hero-text">
            <p class="hero-introduction">Hei, mitt navn er</p>
            <h1 class="hero-name"> {{ yourName }}</h1>
            <h2 class="hero-mini-pitch"> {{ miniPitch }}</h2>
        </div>
        <figure class="hero-image-container">
            <img class="hero-image" v-bind:src="imagePath" v-bind:alt="yourName + '\'s avatar'">
        </figure>
    </section>
    <a class="arrow-down" @click="scrollToSection($event, 'projectPage')">
        <img class="" src="/Arrow-down.svg" alt="Scroll down">
    </a>
</template>

<style scoped>
.arrow-down {
    position: absolute;
    bottom: 0%;
    left: 50%;
    transform: translateX(-50%);
    animation: bounce 1s infinite;
}

.arrow-down img {
    width: 3rem;
}

@keyframes bounce {
    0% {
        transform: translateX(-50%) translateY(0);
    }

    50% {
        transform: translateX(-50%) translateY(4px);
    }

    100% {
        transform: translateX(-50%) translateY(0);
    }
}

.hero {
    display: flex;
    flex-direction: column;
    align-items: center;
    justify-content: center;
    gap: 2rem;
    width: 100%;
    padding: 0 1rem;
    height: 100dvh;
}


.hero-introduction {
    font-size: 1rem;
    font-weight: 400;
    margin: 0;
}

.hero-name {
    font-size: 3rem;
    font-weight: 700;
    margin: 0;
    margin-bottom: 1rem;
}

.hero-mini-pitch {
    font-size: 1rem;
    font-weight: 400;
    margin: 0;
}

.hero-image {
    border-radius: 100%;
    width: 200px;
    height: 200px;
    object-fit: cover;
    border: 0;
    object-position: 0;
}

@media screen and (min-width: 768px) {
    .hero {
        flex-direction: row;
        justify-content: space-between;
        height: 100dvh;
        /* width: 100%; */
        padding: 0;
    }

    .hero-text {
        display: flex;
        flex-direction: column;
        justify-content: center;
        align-items: flex-start;
        max-width: 36rem;
    }

    .hero-image-container {
        display: flex;
        justify-content: center;
        align-items: center;
    }

    .hero-image {
        width: 250px;
        height: 250px;
    }

}

@media screen and (min-width: 1112px) {}
</style>