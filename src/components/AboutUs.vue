<template>
	<div class="main-container">
		<div class="main" data-aos="fade-up" data-aos-easing="ease-in-sine">
			<div class="top">
				<div class="text-container">
					<h1>About us</h1>
					<p>
						At EduFlex, we believe that education should be accessible,
						flexible, and tailored to meet the needs of every learner.
					</p>
				</div>

				<div>
					<img src="/assets/Footer-illustration.svg" alt="Student smiling" />
				</div>
			</div>
			<button class="about-btn">Read all</button>
		</div>
	</div>
</template>
<style scoped>
	.main-container {
		/* padding-top: 10rem; */
		display: flex;
		justify-content: center;
		background-color: #f9f5f2;
		position: relative;
		height: 300px;
	}
	.text-container {
		padding-right: 1rem;
	}
	@media (max-width: 768px) {
		.text-container {
			padding-right: 0px !important;
		}
		.main,
		.top {
			display: flex;
			flex-direction: column;
			justify-content: center;
			align-items: center;
		}
		.top > div {
			text-align: center;
		}

		button {
			margin-top: 1.5rem;
			margin-bottom: 0px;
			width: 130px;
		}
		img {
			width: 100%;
		}
	}

	.main {
		background-color: #f9f5f2;
		box-shadow: 4.5px 4.5px 4px #000000;
		position: absolute;
		bottom: -50%;
		/* top: -50%; */
		border: 2px solid black;
		padding: 2rem;
		width: 70%;
		min-width: 290px;
		max-width: 700px;
	}
	.top {
		display: flex;
		align-items: center;
		justify-content: space-between;
	}
	.top > div {
		height: fit-content;
	}

	img {
		height: 205px;
	}
	button {
		border: 0.5px solid black;
		color: black;
		background-color: transparent;
		padding-left: 2rem;
		padding-right: 2rem;
		padding-top: 1rem;
		padding-bottom: 1rem;
		width: 107px;
	}
</style>
