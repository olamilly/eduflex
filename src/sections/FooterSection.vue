<template>
	<main>
		<div class="text-bar">
			<div class="brand">
				<p>EduFlex</p>
			</div>
			<div
				class="d-flex justify-content-evenly align-items-center footer-links"
			>
				<p class="fw-bolder cursor-pointer">Home</p>
				<p class="fw-bolder">Courses</p>
				<p class="fw-bolder">Community</p>
				<p class="fw-bolder">About</p>
			</div>
			<div class="d-flex justify-content-evenly align-items-center">
				<p class="text-center">Terms & Conditions</p>
				<p class="text-center">© EduFlex 2024</p>
			</div>
		</div>
	</main>
</template>
<style scoped>
	.footer-links {
		cursor: pointer;
	}
	main {
		background-color: #f2c161;
		height: 300px;
		bottom: 0;
	}
	.brand > p {
		font-weight: 700;
		font-size: 19px;
		/* margin-left: 1rem; */
	}
	p {
		margin-left: 1rem;
		margin-right: 1rem;
		margin-bottom: 0;
	}
	.text-bar {
		width: 100%;
		display: flex;
		justify-content: space-between;
		align-items: center;
		position: absolute;
		left: 0;
		bottom: 0;
		padding: 1rem;
		color: #1e1e1e !important;
	}
	@media (max-width: 637px) {
		.text-bar {
			flex-direction: column;
			gap: 1rem;

			/* margin-bottom: 2rem; */
		}
	}
</style>
