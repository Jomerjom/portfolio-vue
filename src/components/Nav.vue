
<script setup>
import { Slide } from 'vue3-burger-menu'  // import the CSS transitions you wish to use, in this case we are using `Slide`
import { ref } from 'vue';

const isOpen = ref(false);

const toggleMenu = () => {
	isOpen.value = !isOpen.value;
};
</script>

<template>
	<Slide right :closeOnNavigation="true">
		<a id="home" href="#">
			<span>Home</span>
		</a>
        <a id="projects" href="#">
			<span>Projects</span>
		</a>
        <a id="about" href="#">
			<span>About</span>
		</a>
        <a id="contact" href="#">
			<span>Contact</span>
		</a>
	</Slide>
</template>

<style scoped>


</style>

