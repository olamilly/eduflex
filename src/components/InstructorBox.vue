<script setup>
	/* eslint-disable */
	const props = defineProps(["thisinstructor"]);
</script>
<template>
	<div class="instructor">
		<img alt="EduFlex Instructor" :src="thisinstructor.img" />

		<div class="details">
			<h3>{{ thisinstructor.name }}</h3>
			<p>{{ thisinstructor.role }}</p>
		</div>
	</div>
</template>
<style scoped>
	.instructor {
		max-width: 300px;
	}
	img {
		width: 100%;
		transition: 0.3s ease-in-out;
		margin-bottom: 1rem;
	}
	img:hover {
		transform: scale(1.08);
	}
</style>
