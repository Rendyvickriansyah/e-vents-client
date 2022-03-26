<template>
	<div class="row">
		<div class="col">
			<h4>{{ title }}</h4>
			<p class="mt-3">{{ subTitle }}</p>
		</div>
	</div>
</template>

<script>
export default {
	name: "TitleSubTitle",
	props: {
		title: String,
		subTitle: String,
	},
};
</script>

<style scoped>
h5 {
	color: #282142;
}

p {
	font-size: 0.9rem;
	color: #8e87ac;
	line-height: 1.5;
}
</style>
