<script setup>

defineProps({
  miniPitch: String,
  yourName: String,
  imagePath: String,
})

</script>

<template>
<div class="hero">
    <div class="hero-text">
        <h2 class="hero-introduction">Hei, mitt navn er</h2>
        <h1 class="hero-name"> {{ yourName }}</h1>
        <p class="hero-mini-pitch"> {{ miniPitch }}</p>
    </div>
    <div class="hero-image-container">
        <img class="hero-image" v-bind:src="imagePath" v-bind:alt="yourName + '\'s avatar'">
    </div>
</div>
</template>

<style scoped>
.hero {
    display: flex;
    flex-direction: column;
    align-items: center;
    justify-content: center;
    gap: 2rem;
    width: 100%;
    padding: 0 1rem;
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
    border: 0;
}

.hero {
    height: 100vh;
}

@media screen and (min-width: 768px) {
    .hero {
        flex-direction: row;
        justify-content: space-between;
        height: 100vh;
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

@media screen and (min-width: 1112px) {

}
</style>