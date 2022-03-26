<template>
	<div class="home text-white">
		<Navbar />
		<Cards />
	</div>
</template>

<script>
import Navbar from "../components/Navbar.vue";
import Cards from "../components/Cards.vue";

export default {
	name: "HomeView",

	components: {
		Cards,
		Navbar,
	},
};
</script>

//
<style>
body {
	background-color: #1f1d2b !important;
}
</style>
