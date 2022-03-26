<template>
	<Navbar />
	<div class="container mb-5">
		<div class="row">
			<div class="col">
				<a
					@click="back"
					class="d-flex align-items-center text-decoration-none text-dark"
					><i class="ri-arrow-left-line ri-xl me-2"></i> Back</a
				>
			</div>
		</div>
		<div class="row mt-5">
			<div class="col col-lg-6 me-auto">
				<TitleSubTitle title="Description" :subTitle="event.description" />
			</div>
			<div class="col col-lg-4">
				<TitleSubTitle title="Event Location" :subTitle="event.location" />
				<BookingEventCard :price="event.price" class="mt-3" />
			</div>
		</div>
	</div>
	<Footer />
</template>

<script>
import Navbar from "../components/Navbar.vue";
import TitleSubTitle from "../components/TitleSubTitle.vue";
import BookingEventCard from "../components/BookingEventCard.vue";
import Footer from "../components/Footer.vue";

export default {
	props: ["id"],

	data() {
		return {
			event: "",
		};
	},
	methods: {
		back() {
			this.$router.back();
		},
	},
	mounted() {
		fetch(`http://localhost:1337/api/events/${this.id}?populate=*`)
			.then((res) => res.json())
			.then((data) => (this.event = data.data.attributes))
			.catch((err) => console.log(err));
	},
	components: {
		Navbar,
		TitleSubTitle,
		BookingEventCard,
		Footer,
	},
};
</script>

<style scoped>
a {
	cursor: pointer;
}
</style>
