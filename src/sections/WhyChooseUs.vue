<script setup>
	// import { Hooper, Slide } from "hooper";
	import * as AOS from "aos";
	AOS.init();
	import ReasonBox from "../components/ReasonBox.vue";

	const reasons = [
		{
			alt: "Student Icon",
			src: "/assets/icons/Student.svg",
			header: "Flexible Learning at Your Pace",
			subtext:
				"EduFlex offers a flexible learning experience that fits your schedule. Whether you're balancing a career, family, or other commitments, our self-paced courses allow you to learn whenever and wherever it's most convenient for you.",
		},
		{
			alt: "Microscope Icon",
			src: "/assets/icons/Microscope.svg",
			header: "Expert-Led Courses",
			subtext:
				"Our courses are designed and taught by industry experts with real-world experience. You'll gain practical skills and knowledge that are directly applicable to your career, helping you stay ahead in a competitive job market.",
		},
		{
			alt: "Book Icon",
			src: "/assets/icons/Book.svg",
			header: "Diverse Course Offerings",
			subtext:
				"With a wide variety of courses across multiple disciplines, EduFlex caters to diverse interests and career goals. Whether you're looking to advance in your current field or explore something new, we have the right course for you.",
		},
	];
</script>
<template>
	<main>
		<h1 data-aos="fade">Achieve your goal with EduFlex</h1>
		<div data-aos="fade" class="d-flex justify-content-center">
			<p>
				It is a long established fact that we offer the best education services
				to our clients without a doubt.
			</p>
		</div>

		<section class="my-5">
			<ReasonBox
				v-for="(reason, index) in reasons"
				:key="index"
				:myreason="reason"
				:id="`reason-${index + 1}`"
				data-aos="fade-up"
				data-aos-duration="900"
				:data-aos-delay="`${index * 2 * 100}`"
			/>
			<!-- <div v-for="(reason, index) in reasons" :key="index" class="reason">
				<div class="icon-box">
					<img :alt="reason.alt" :src="reason.src" />
				</div>
				<div>
					<h3>{{ reason.header }}</h3>
					<p>{{ reason.subtext }}</p>
				</div>
			</div> -->
		</section>
	</main>
</template>
<style lang="css" scoped>
	main {
		background-color: #f9f5f2;
		padding: 3rem;
	}

	h1 {
		text-align: center;
	}
	main > div > p {
		max-width: 505px;
		text-align: center;
	}
	section {
		display: flex;
		justify-content: center;
		flex-wrap: wrap;
		gap: 2rem;
	}
	@media (min-width: 652px) and (max-width: 949px) {
		#reason-3 {
			width: calc(540px + 2rem);
		}
	}
</style>
