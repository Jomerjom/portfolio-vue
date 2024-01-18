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
    <div class="about-wrapper">
        <div class="about-text">
            <h1>About Me</h1>
            <p>{{ pitchP1 }}</p>
            <p>{{ pitchP2 }}</p>
        </div>
            <img class="about-image" :src="imagePath" alt="Portrait">
    </div>
    <div class="toolkit">
        <h2>Toolkit</h2>
        <div class="toolkit-container">
            <div v-for="item in toolkitItems" :key="item.name" class="toolkit-item">
                <img :src="item.image" :alt="item.name">
                <p>{{ item.name[0].toUpperCase() + item.name.substring(1) }}</p>
            </div>
        </div>
    </div>
</template>

<style scoped>

.about-wrapper {
    display: flex;
    flex-direction: row;
    align-items: center;
    justify-content: space-between;
    width: 100%;
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
    width: 120px;
    margin: 0 20px;
    padding: 20px 0; 
    gap: 10px;
}

.toolkit-item img {
    width: 50px;
    height: 50px;
    object-fit: contain;
}
</style>
