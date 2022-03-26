<template>
	<button>{{ buttonTitle }}</button>
</template>

<script>
export default {
	props: {
		buttonTitle: String,
	},
};
</script>

<style>
button {
	background-color: #5465ff;
	color: #fff;
	padding: 12px 0;
	border-radius: 10px !important;
	border: none;
	box-shadow: 0 1px 2px rgba(0, 0, 0, 0.15);
	transition: box-shadow 0.3s ease-in-out;
}

button:hover {
	background-color: #3a49ca;
	box-shadow: 0 5px 15px rgba(0, 0, 0, 0.3);
}
</style>
