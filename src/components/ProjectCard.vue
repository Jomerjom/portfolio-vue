<script setup>
defineProps({
    projectName: String,
    projectDescription: String,
    projectViewLink: String,
    projectGitLink: String,
    imagePath: String,
});
</script>

<template>
    <div class="project-card" :style="{ backgroundImage: 'url(' + imagePath + ')' }">
        <div class="project-card-info">
            <h2 class="project-card-name">{{ projectName }}</h2>
            <p class="project-card-description">{{ projectDescription }}</p>
            <div>
                <a class="project-card-view-link" v-bind:href="projectViewLink">
                    <button class="project-card-button">View Live</button>
                </a>
                <a class="project-card-git-link" v-bind:href="projectGitLink">
                    <button class="project-card-button">GitHub</button>
                </a>
            </div>
        </div>
    </div>
</template>

<style scoped>
.project-card {
    display: flex;
    flex-direction: column;
    align-items: center;
    justify-content: center;
    background-position: center;
    background-repeat: no-repeat;
    background-size: cover;
    width: 100%;
    height: 100%;
    text-align: center;
    border-radius: 0.5rem;
}

.project-card-info {
    background: rgba(0, 0, 0, 0.75);
    width: 100%;
    height: 100%;
    border-radius: 0.5rem;
    opacity: 0;
    display: flex;
    flex-direction: column;
    align-items: center;
    justify-content: center;
    gap: 1rem;
    padding: 1rem; 
    transition: opacity 0.3s ease-in-out;
}

.project-card-info:hover {
    opacity: 1;
}

h2 {
    font-size: 1.5rem;
    font-weight: 700;
    margin: 0;
    color: white;
}

p {
    font-size: 1rem;
    font-weight: 400;
    margin: 0;
    color: white;
}

button {
    font-size: 1rem;
    font-weight: 700;
    margin: 0;
    color: white;
    background: none;
    border: 2px solid white;
    border-radius: 0.5rem;
    padding: 0.5rem 1rem;
    margin: 0.5rem;
    cursor: pointer;
}


</style>
