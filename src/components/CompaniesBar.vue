<template>
	<div class="slider w-100">
		<div class="slide-track">
			<div class="slide">
				<img alt="company logo" src="/assets/companies/google.svg" />
			</div>
			<div class="slide">
				<img alt="company logo" src="/assets/companies/airbnb.svg" />
			</div>
			<div class="slide">
				<img alt="company logo" src="/assets/companies/allstate.svg" />
			</div>
			<div class="slide">
				<img alt="company logo" src="/assets/companies/axon.svg" />
			</div>
			<div class="slide">
				<img alt="company logo" src="/assets/companies/google.svg" />
			</div>
			<div class="slide">
				<img alt="company logo" src="/assets/companies/airbnb.svg" />
			</div>
			<div class="slide">
				<img alt="company logo" src="/assets/companies/allstate.svg" />
			</div>
			<div class="slide">
				<img alt="company logo" src="/assets/companies/axon.svg" />
			</div>
			<div class="slide">
				<img alt="company logo" src="/assets/companies/airbnb.svg" />
			</div>
			<div class="slide">
				<img alt="company logo" src="/assets/companies/allstate.svg" />
			</div>
			<div class="slide">
				<img alt="company logo" src="/assets/companies/axon.svg" />
			</div>
		</div>
	</div>
</template>
<style lang="css" scoped>
	main {
		width: 100%;
		padding: 1rem;
		display: flex;
		justify-content: space-evenly;
		align-items: center;
		flex-wrap: wrap;
	}
	main > img {
		padding: 0.7rem;
	}
	@keyframes scroll {
		0% {
			transform: translateX(0);
		}
		100% {
			transform: translateX(calc(-250px * 5));
		}
	}
	.slider {
		background-color: black;
		/* box-shadow: 0 10px 20px -5px rgba(0, 0, 0, 0.125); */
		/* height: 100px; */
		margin: auto;
		overflow: hidden;
		position: relative;
		width: 100%;
	}
	.slider::before,
	.slider::after {
		/* background: linear-gradient(
			to right,
			rgba(255, 255, 255, 1) 0%,
			rgba(255, 255, 255, 0) 100%
		); */
		content: "";
		/* height: 100px; */
		position: absolute;
		width: 200px;
		z-index: 2;
	}
	.slider::after {
		right: 0;
		top: 0;
		transform: rotateZ(180deg);
	}
	.slider::before {
		left: 0;
		top: 0;
	}
	.slider .slide-track {
		animation: scroll 30s linear infinite;
		display: flex;
		/* justify-content: space-evenly; */
		width: 1000px;
	}
	.slider .slide {
		/* height: 100px;
		width: 250px; */
		margin-left: 2rem;
		margin-right: 2rem;
		margin-top: 1.7rem;
		margin-bottom: 1.7rem;
	}
</style>
