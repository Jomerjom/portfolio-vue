<script setup>
import ProjectCard from './ProjectCard.vue';

</script>

<template>
    <div class="project-row">
        <ProjectCard class="projectCard-one ProjectCard" projectName="Test Project" projectDescription="A Vite vue project component, to show of your skills on your portfolio!" imagePath="/public/project-placeholder.png" />
        <ProjectCard class="projectCard-two ProjectCard" projectName="Test Project" projectDescription="A Vite vue project component, to show of your skills on your portfolio!" imagePath="/public/project-placeholder.png" />
    </div>
    <div class="project-row">
        <ProjectCard class="projectCard-three ProjectCard" projectName="Test Project" projectDescription="A Vite vue project component, to show of your skills on your portfolio!" imagePath="/public/project-placeholder.png" />
        <ProjectCard class="projectCard-four ProjectCard" projectName="Test Project" projectDescription="A Vite vue project component, to show of your skills on your portfolio!" imagePath="/public/project-placeholder.png" />
    </div>

</template>


<style scoped>
.project-row {
    display: flex;
    flex-direction: column;
    align-items: center;
    justify-content: center;
    width: 100%;
}

.ProjectCard {
    height: 350px;
    margin: 1rem 0;
}

@media screen and (min-width: 768px) {
    .project-row {
        flex-direction: row;
        gap: 2rem;
    }

    .ProjectCard {
        width: 50%;
        height: 400px;
    }
    
}

</style>