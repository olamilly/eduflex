<script setup>
	/* eslint-disable */
	const props = defineProps(["mycourse"]);
</script>
<template>
	<div class="course">
		<small class="tag">{{ mycourse.tag }}</small>
		<h5 class="name my-2">
			{{ mycourse.name }}
		</h5>
		<div class="d-flex justify-content-between align-items-center my-3">
			<div class="d-flex justify-content-center align-items-center">
				<img alt="Course Instructor" :src="mycourse.img" />
				<p class="mb-0 ms-2">{{ mycourse.instructor }}</p>
			</div>
			<small class="sessions">{{ mycourse.sessions }} Sessions</small>
		</div>
		<div class="d-flex justify-content-between align-items-center">
			<p class="mb-1 price">${{ mycourse.price }}</p>
			<p class="d-flex justify-content-center align-items-center mb-1 rating">
				<img alt="Star Icon" src="/assets/icons/Star.svg" /><span
					class="ms-1"
					>{{ mycourse.rating }}</span
				>
			</p>
		</div>
	</div>
</template>
<style scoped>
	h5 {
		text-align: center;
	}
	.sessions {
		color: #959595;
		font-weight: 500;
	}
	.tag {
		color: #959595;
		font-weight: 300;
	}
	.course {
		width: 30%;
		min-width: 270px;
		background-color: white;
		max-width: 387px;
		border: 1px solid black;
		outline: none;
		padding: 10px;
		box-shadow: 3px 3px 4px #000000;
		cursor: pointer;
	}
	.price,
	.rating > span {
		font-weight: 600;
	}
</style>
