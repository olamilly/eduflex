<template>
	<div class="position-relative">
		<HeroSection />
		<WhyChooseUs />
		<CoursesOffered />
		<InstructorProfiles />
		<StudentTestimonials />
		<AboutUs />
		<FooterSection />
	</div>
</template>

<script setup>
	import CoursesOffered from "./sections/CoursesOffered.vue";
	import HeroSection from "./sections/HeroSection.vue";
	import WhyChooseUs from "./sections/WhyChooseUs.vue";
	import InstructorProfiles from "./sections/InstructorProfiles.vue";
	import StudentTestimonials from "./sections/StudentTestimonials.vue";
	import FooterSection from "./sections/FooterSection.vue";
	import AboutUs from "@/components/AboutUs.vue";
</script>

<style>
	* {
		/* font-family: "Inter", sans-serif; */
		font-family: "Outfit", sans-serif;
		font-optical-sizing: auto;
		font-style: normal;
		font-weight: 400;
		font-size: 14px;
		color: #1e1e1e;
	}
	.shadow-btn {
		background-color: #f2c161;
		border: 1px solid black;
		outline: none;
		padding: 10px;
		box-shadow: 3px 3px 4px #000000;
	}
	input {
		background-color: white;
		border: 1px solid black;
		outline: none;
		padding: 10px;
		box-shadow: 3px 3px 4px #000000;
		width: 60%;
		max-width: 350px;
	}
	.b-lg {
		width: 126px;
	}
	.b-sm {
		width: 77px;
	}
	.shadow-btn:hover,
	.course:hover,
	.transparent-btn:hover,
	.about-btn:hover {
		transform: translateY(-3px);
	}
	.transparent-btn {
		border: 2px solid #f2c161;
		outline: none;
		background-color: transparent;
		color: #f2c161;
		padding-left: 1.5rem;
		padding-right: 1.5rem;
		padding-top: 0.5rem;
		padding-bottom: 0.5rem;
		width: 200px;
	}
</style>
