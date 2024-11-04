<template>
	<main>
		<h1 data-aos="fade-up" data-aos-easing="ease-in-sine">
			Hear From Our Learners
		</h1>
		<section
			class="my-4"
			data-aos="fade-up"
			data-aos-easing="ease-in-sine"
			data-aos-delay="200"
		>
			<div class="d-flex align-items-center justify-content-center">
				<div class="slideshow-container">
					<div class="img-row">
						<img
							class="navigation-dot"
							@click="currentSlide(1)"
							src="/assets/course-instructors/instructor3.jpg"
						/>

						<img
							class="navigation-dot"
							@click="currentSlide(2)"
							src="/assets/course-instructors/instructor1.jpg"
						/>
						<img
							class="navigation-dot"
							@click="currentSlide(3)"
							src="/assets/course-instructors/instructor2.jpg"
						/>
					</div>
					<div class="mySlides">
						<div class="slidebox fade">
							<div>
								<p>
									“The courses on this platform have completely transformed my
									career! The flexible learning schedule allowed me to study at
									my own pace, and the quality of instruction was top-notch.
									After completing the 'Data Science Mastery' course, I landed a
									job as a Data Analyst at a leading tech company. I couldn't be
									more grateful for the knowledge and confidence I've gained.”
								</p>
								<div
									class="d-flex flex-column align-items-center justify-content-center testimonial-bio"
								>
									<h3>Zinachidi Nwachukwu</h3>
									<p class="mb-0">Data Scientist</p>
								</div>
							</div>
						</div>
					</div>

					<div class="mySlides">
						<div class="slidebox fade">
							<div>
								<p>
									This e-learning platform provided everything I needed to
									advance my career in cloud technology. The 'Cloud Engineering
									Essentials' course was comprehensive, with real-world
									scenarios and expert guidance. The ability to learn at my own
									pace made it easy to balance work and study. Within months of
									completing the course, I earned a job as a Cloud Engineer at a
									major tech company. I'm grateful for the clear, structured
									learning path that led to my success.
								</p>
								<div
									class="d-flex flex-column align-items-center justify-content-center testimonial-bio"
								>
									<h3>Don Toliver</h3>
									<p class="mb-0">Cloud Solutions Architect</p>
								</div>
							</div>
						</div>
					</div>

					<div class="mySlides">
						<div class="slidebox fade">
							<div>
								<p>
									“The courses on this platform have been a game-changer for my
									career! The in-depth curriculum and hands-on projects gave me
									the practical experience I needed. The flexible learning
									schedule fit perfectly into my busy life, allowing me to
									complete the 'Full-Stack Developer' course. Shortly after, I
									secured a position as a Software Developer at a top startup.
									The skills and confidence I gained were invaluable, and I'm
									excited about my future in tech.”
								</p>
								<div
									class="d-flex flex-column align-items-center justify-content-center testimonial-bio"
								>
									<h3>Jocelyn Flores</h3>
									<p class="mb-0">Software Developer</p>
								</div>
							</div>
						</div>
					</div>

					<a class="prev" @click="plusSlides(-1, 'r')"
						><i class="bx bx-chevron-left"></i
					></a>
					<a class="next" @click="plusSlides(1, 'l')"
						><i class="bx bx-chevron-right"></i
					></a>
				</div>
				<br />
			</div>
		</section>
	</main>
</template>
<script setup>
	import * as AOS from "aos";
	import { onMounted, ref } from "vue";
	AOS.init();
	//Js code for testimonial carousel control
	let slideIndex = ref(2);
	function plusSlides(n) {
		showSlides((slideIndex.value += n));
	}

	function currentSlide(n) {
		showSlides((slideIndex.value = n));
	}

	function showSlides(n) {
		let i;
		let slides = document.getElementsByClassName("mySlides");
		var dots = document.getElementsByClassName("navigation-dot");
		if (n > slides.length) {
			slideIndex.value = 1;
		}
		if (n < 1) {
			slideIndex.value = slides.length;
		}
		for (i = 0; i < slides.length; i++) {
			slides[i].style.display = "none";
		}
		for (i = 0; i < dots.length; i++) {
			dots[i].className = dots[i].className.replace(" active", "");
		}
		// slides[slideIndex.value - 1].classList.remove("fade-in-left");
		// slides[slideIndex.value - 1].classList.remove("fade-in-right");
		// if (f == "l") {
		// 	slides[slideIndex.value - 1].classList.add("fade-in-right");
		// } else {
		// 	slides[slideIndex.value - 1].classList.add("fade-in-left");
		// }
		slides[slideIndex.value - 1].style.display = "block";
		dots[slideIndex.value - 1].className += " active";
	}
	onMounted(() => {
		showSlides(slideIndex.value);
	});
</script>
<style lang="css" scoped>
	.navigation-dot {
		cursor: pointer;
		display: inline-block;
		transition: 0.6s ease;
		/* border: 1px solid black; */
		width: 50px;
		height: 50px;
		border-radius: 50%;
		box-shadow: 0 4px 8px rgba(0, 0, 0, 0.2);
		/* filter: grayscale(100%); */
		opacity: 0.7;
	}
	img {
		width: 100%;
		height: 100%;
		object-fit: cover;
	}
	.active {
		transform: scale(1.6);
		z-index: 3;
		opacity: 1;
		border: 1px solid white;
	}
	.img-row {
		display: flex;
		justify-content: center;
		transform: translateY(20px);
	}
	.testimonial-bio > p {
		color: #8e8888;
		font-size: 10px;
	}
	.testimonial-bio > h3 {
		text-align: center;
	}
	p {
		text-align: center;
	}
	main {
		background-color: #f9f5f2;
		padding: 3rem;
	}
	h1 {
		text-align: center;
		margin-bottom: 2rem;
	}
	.mySlides {
		display: none;

		margin-bottom: 2rem;
		background-color: white;
		border: 1px solid black;
		box-shadow: 4.5px 4.5px 4px #000000;
		/* min-height: 300px; */
		animation-timing-function: ease;
	}
	.slidebox {
		vertical-align: middle;
		display: flex;

		justify-content: center;
		padding: 2.5rem;
	}
	.slidebox > div {
		width: 100%;
		max-width: 400px;
		display: flex;
		flex-direction: column;
		align-items: center;
		justify-content: center;
	}

	/* Slideshow container */
	.slideshow-container {
		max-width: 700px;
		min-width: 290px;
		width: 85%;
		position: relative;
		/* margin: auto; */
		/* margin-bottom: 40%; */
	}
	.bx {
		font-size: 23px;
	}
	/* Next & previous buttons */
	@media (max-width: 500px) {
		.prev,
		.next {
			height: 30px !important;
			width: 30px !important;
		}
		.next {
			right: -1rem !important;
		}
		.prev {
			left: -1rem !important;
		}
		.slideshow-container {
			width: 100%;
		}
	}
	.prev,
	.next {
		cursor: pointer;
		position: absolute;
		top: 50%;
		/* width: auto; */
		/* padding: 16px; */
		height: 45px;
		width: 45px;
		margin-top: -22px;
		/* font-weight: bold;
		font-size: 10px; */
		background-color: #ecebff;
		border-radius: 50%;
		border: 0.8px solid black;
		display: flex;
		justify-content: center;
		align-items: center;
		text-decoration: none;
		user-select: none;
	}
	/* Position the "next button" to the right */
	.next {
		right: -1.5rem;
	}
	.prev {
		left: -1.5rem;
	}

	/* Fading animation */
	.fade {
		animation-name: fade;
		animation-duration: 1.5s;
		animation-fill-mode: forwards;
	}

	@keyframes fade {
		from {
			/* transform: translateX(10%); */
			opacity: 0;
		}
		to {
			/* transform: translateX(0%); */
			opacity: 1;
		}
	}
</style>
