<script setup>
import ProjectCard from './ProjectCard.vue';

</script>

<template>
    <div class="project-wrapper">
        <p class="description">Hover over a project to learn more</p>
        <div class="project-row">
            <ProjectCard class="projectCard-one ProjectCard" projectName="Test Project"
                projectDescription="A Vite vue project component, to show of your skills on your portfolio!"
                imagePath="/public/project-placeholder.png" />
            <ProjectCard class="projectCard-two ProjectCard" projectName="Test Project"
                projectDescription="A Vite vue project component, to show of your skills on your portfolio!"
                imagePath="/public/project-placeholder.png" />
        </div>
        <div class="project-row">
            <ProjectCard class="projectCard-three ProjectCard" projectName="Test Project"
                projectDescription="A Vite vue project component, to show of your skills on your portfolio!"
                imagePath="/public/project-placeholder.png" />
            <ProjectCard class="projectCard-four ProjectCard" projectName="Test Project"
                projectDescription="A Vite vue project component, to show of your skills on your portfolio!"
                imagePath="/public/project-placeholder.png" />
        </div>
    </div>
</template>


<style scoped>
.project-wrapper {
    display: flex;
    flex-direction: column;
    align-items: flex-start;
    justify-content: flex-start;
}

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
    width: 100%;
}

@media screen and (min-width: 768px) {
    .project-row {
        flex-direction: row;
        gap: 2rem;
    }

    .ProjectCard {
        width: 50%;
        height: 350px;
    }

    .projectCard-one {
        width: 60%;
    }

    .projectCard-two {
        width: 40%;
    }

    .projectCard-three {
        width: 40%;
    }

    .projectCard-four {
        width: 60%;
    }
}
</style>