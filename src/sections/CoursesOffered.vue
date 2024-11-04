<script setup>
	import CourseBox from "@/components/CourseBox.vue";
	import * as AOS from "aos";
	AOS.init();
	const courses = [
		{
			img: "/assets/course-instructors/Anette.svg",
			instructor: "Anette Black",
			tag: "Graphic Design",
			name: "The complete graphic design theory for beginners course",
			sessions: "21",
			price: "18.00",
			rating: "5",
		},
		{
			img: "/assets/course-instructors/Cameron.svg",
			instructor: "Cameron Williamson",
			tag: "Web Development",
			name: "Mastering HTML, CSS, and JavaScript for Beginners",
			sessions: "15",
			price: "25.00",
			rating: "4.5",
		},
		{
			img: "/assets/course-instructors/Kristin.svg",
			instructor: "Kristin Watson",
			tag: "Photography",
			name: "Fundamentals of Digital Photography",
			sessions: "10",
			price: "20.00",
			rating: "4.8",
		},
		{
			img: "/assets/course-instructors/Diane.svg",
			instructor: "Diane Russel",
			tag: "Programming",
			name: "Python for Beginners",
			sessions: "20",
			price: "40.00",
			rating: "4.7",
		},
		{
			img: "/assets/course-instructors/Esther.svg",
			instructor: "Esther Howard",
			tag: "Art",
			name: "Introduction to Sculpting",
			sessions: "8",
			price: "28.00",
			rating: "4.8",
		},
		{
			img: "/assets/course-instructors/Arlene.svg",
			instructor: "Arlene McCoy",
			tag: "Cooking",
			name: "Mastering Italian Cuisine",
			sessions: "15",
			price: "30.00",
			rating: "4.9",
		},
	];
</script>
<template>
	<main>
		<h1 data-aos="fade-up">In demand courses</h1>
		<div class="search-bar my-4 d-flex" data-aos="fade">
			<input placeholder="Search Course" />
			<button class="shadow-btn b-sm fw-bolder">Search</button>
		</div>
		<section data-aos="fade-up" data-aos-delay="100" data-aos-duration="900">
			<div class="d-flex flex-wrap justify-content-center gap-3">
				<CourseBox
					v-for="(course, index) in courses"
					:key="index"
					:mycourse="course"
					:id="`box-${index}`"
				/>
			</div>
			<!-- <div class="gap-3 mt-3 bottom-row">
				<CourseBox
					v-for="(course, index) in courses.slice(3, 6)"
					:key="index"
					:mycourse="course"
				/>
			</div> -->
			<p class="more my-4">
				<span class="fw-bolder mb-1">More Courses</span
				><span><i class="bx bx-right-arrow-alt"></i></span>
			</p>
		</section>
	</main>
</template>
<style scoped>
	main {
		background-color: #ecebff;
		padding: 3rem;
	}
	.search-bar {
		justify-content: center;
		gap: 1rem;
		align-items: center;
	}
	h1 {
		text-align: center;
	}
	.more {
		display: none;
	}

	@media (max-width: 637px) {
		.more {
			display: flex;
			justify-content: center;
			align-items: center;
			cursor: pointer;
		}
		.more:hover {
			text-decoration: underline;
		}
		#box-3,
		#box-4,
		#box-5 {
			display: none;
		}
	}
</style>
