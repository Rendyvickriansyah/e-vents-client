<template>
	<div class="home">
		<Navbar />
		<Banner />
		<Cards />
		<Footer />
	</div>
</template>

<script>
import Navbar from "../components/Navbar.vue";
import Banner from "../components/Banner.vue";
import Cards from "../components/Cards.vue";
import Footer from "../components/Footer.vue";

export default {
	name: "HomeView",

	components: {
		Navbar,
		Cards,
		Banner,
		Footer,
	},
};
</script>

//
<style>
body {
	background-color: #f5f5f5 !important;
}
</style>
