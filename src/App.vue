<script setup>
import Hero from './components/Hero.vue'
import ResponsiveNav from './components/ResponsiveNav.vue';
import ProjectShowing from './components/ProjectShowing.vue';

</script>

<template>
  <ResponsiveNav />
  <main>
    <Hero
      miniPitch="Lorem ipsum dolor sit amet, consectetur adipiscing elit. Sed sed metus erat. Proin aliquet facilisis justo vel fringilla. Praesent eu tellus in dui gravida pharetra. Ut posuere purus quis neque."
      yourName="Joachim" imagePath="/avatar-placeholder.webp" />
    <ProjectShowing />
  </main>
</template>

<style scoped>
main {
  padding: 0 1rem;
  display: flex;
  flex-direction: column;
}

@media (min-width: 768px) {
  main {
    max-width: 1080px;
    width: 100%;
    display: flex;
    padding: 0;
  }
}
</style>