<script setup>
import skills from '../assets/skills.json';

defineProps({
    pitchP1: String,
    pitchP2: String,
    imagePath: String,
});

const toolkitItems = skills.map(skill => ({
    name: skill.name,
    image: skill.logoPath,
}));
</script>

<template>
    <section class="about-toolkit">
        <div class="about-wrapper">
            <article class="about-text">
                <h2>About Me</h2>
                <p>{{ pitchP1 }}</p>
                <br>
                <p>{{ pitchP2 }}</p>
            </article>
            <img class="about-image" :src="imagePath" alt="Portrait">
        </div>
        <div class="toolkit">
            <h2>Toolkit</h2>
            <div class="toolkit-container">
                <figure v-for="item in toolkitItems" :key="item.name" class="toolkit-item">
                    <img :src="item.image" :alt="item.name">
                    <p>{{ item.name[0].toUpperCase() + item.name.substring(1) }}</p>
                </figure>
            </div>
        </div>
    </section>
</template>

<style scoped>

.about-toolkit {
    display: flex;
    flex-direction: column;
    align-items: center;
    justify-content: center;
    gap: 6rem;
    width: 100%;
}

.about-wrapper {
    display: flex;
    flex-direction: column;
    align-items: center;
    justify-content: space-between;
    width: 100%;
    gap: 6rem;
}

@media screen and (min-width: 768px) {
    .about-wrapper {
        flex-direction: row;
        align-items: flex-start;
    }

}

.about-image {
    border-radius: 5%;
    max-width: 350px;
    height: calc(width * 1.18);
    object-fit: cover;
}

.toolkit-container {
    display: flex;
    flex-wrap: wrap;
    justify-content: center;
}

.toolkit-item {
    display: flex;
    flex-direction: column;
    align-items: center;
    justify-content: center;
    width: 80px;
    margin: 0;
    padding: 20px 0;
    gap: 10px;
}

.toolkit-item img {
    width: 50px;
    height: 50px;
    object-fit: contain;
}

@media screen and (min-width: 768px) {
    .toolkit-item {
        width: 120px;
        margin: 0 20px;
        padding: 20px 0;
    }
}
</style>
