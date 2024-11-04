<script setup>
	/* eslint-disable */
	const props = defineProps(["myreason"]);
</script>
<template>
	<div class="reason">
		<div class="icon-box">
			<img :alt="myreason.alt" :src="myreason.src" />
		</div>
		<div>
			<h3>{{ myreason.header }}</h3>
			<p>{{ myreason.subtext }}</p>
		</div>
	</div>
</template>
<style scoped>
	.reason {
		background-color: white;
		padding: 1.5rem;
		box-shadow: 6.5px 6.5px 4px #000000;
		width: 30%;
		min-width: 270px;
	}
	.icon-box {
		background-color: #f9f5f2;
		padding: 1rem;
		width: fit-content;
	}
</style>
