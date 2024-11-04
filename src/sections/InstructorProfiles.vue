<template>
	<main>
		<h1>Meet some of our top instructors</h1>
		<section class="my-4">
			<div class="d-flex flex-wrap justify-content-center gap-3">
				<InstructorBox
					v-for="(instructor, index) in instructors"
					:key="index"
					:thisinstructor="instructor"
					data-aos="fade-up"
					data-aos-easing="ease-in-sine"
					:data-aos-delay="200"
				/>
			</div>
		</section>
		<div
			class="d-flex justify-content-center align-items-center w-100 my-3"
			data-aos="fade-up"
			data-aos-easing="ease-in-sine"
		>
			<button class="transparent-btn">See All</button>
		</div>
	</main>
</template>
<script setup>
	import InstructorBox from "@/components/InstructorBox.vue";
	import * as AOS from "aos";
	AOS.init();
	/* eslint-disable */
	const instructors = [
		{
			img: "/assets/course-instructors/instructor1.jpg",
			name: "Robert Fox",
			role: "Team Leader",
		},
		{
			img: "/assets/course-instructors/instructor2.jpg",
			name: "Jenny Wilson",
			role: "Software Development Manager",
		},
		{
			img: "/assets/course-instructors/instructor3.jpg",
			name: "Arlene McCoy",
			role: "Scrum Master",
		},
		{
			img: "/assets/course-instructors/instructor4.jpg",
			name: "Breanna Williams",
			role: "UI/UX Designer",
		},
		{
			img: "/assets/course-instructors/instructor5.jpg",
			name: "Cameron Williamson",
			role: "Software Developer",
		},
		{
			img: "/assets/course-instructors/instructor6.jpg",
			name: "Alberta Flores",
			role: "Project Manager",
		},
	];
</script>
<style lang="css" scoped>
	main {
		background-color: #f9f5f2;
		padding: 3rem;
	}
	h1 {
		text-align: center;
	}
</style>
