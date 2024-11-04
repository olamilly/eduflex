<script setup>
	import Header from "../components/HeaderComp.vue";
	import Companies from "@/components/CompaniesBar.vue";
	import * as AOS from "aos";
	AOS.init();
</script>
<template>
	<section
		class="hero"
		data-aos="fade"
		data-aos-easing="ease-in-sine"
		data-aos-duration="900"
		data-aos-once="true"
	>
		<Header />
		<main class="d-flex">
			<div class="headline-container">
				<h1>Online learning <span>wherever</span> and <span>whenever</span></h1>
				<p>
					We bring education to your fingertips. Whether you're at home, on the
					go, or juggling multiple responsibilities, our platform gives you the
					freedom to learn at your own pace, on your own schedule.
				</p>
				<button class="shadow-btn b-lg fw-bolder">Get Started</button>
			</div>
			<div class="illustration-container">
				<img alt="Student Illustration" src="/assets/Hero-illustration.svg" />
			</div>
		</main>
		<Companies />
	</section>
</template>
<style scoped>
	h1 {
		font-weight: 700;
		font-size: 48px;
	}
	img {
		max-width: 100%;
	}
	.hero {
		background-color: #f9f5f2;
		display: flex;
		flex-direction: column;
		/* flex-wrap: wrap; */
	}
	main {
		flex-grow: 1;
	}

	.illustration-container {
		background-color: #ffa5a6;
		display: flex;
		justify-content: center;
		align-items: center;
	}
	.headline-container {
		display: flex;
		flex-direction: column;
		justify-content: center;
		align-items: flex-start;
		gap: 1.5em;
		padding: 3rem;
	}
	.headline-container > p {
		width: 90%;
	}
	h1 > span {
		font-size: inherit;
		font-weight: inherit;
		color: #ffa5a6;
	}
	@media (min-width: 576px) {
		main > div {
			width: 50% !important;
		}
	}
	@media (max-width: 576px) {
		/* main {
			flex-direction: column;
		} */

		.headline-container {
			padding: 3rem;
			text-align: center;
			/* height: 50dvh; */
		}
		.headline-container > button {
			align-self: center;
		}

		.headline-container > p {
			width: 100%;
		}

		.illustration-container {
			display: none;
			width: 100%;
			padding: 1rem;
		}
		.hero {
			min-height: 100dvh;
		}
	}
</style>
