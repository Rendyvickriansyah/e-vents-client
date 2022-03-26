<template>
	<div class="card border-0 p-4 shadow-sm">
		<h5 class="text-uppercase">Price</h5>
		<p class="fw-bolder">{{ price }}</p>
		<!-- <button class="btn-booking">Booking now</button> -->
		<Button buttonTitle="Booking Now" />
	</div>
</template>

<script>
import Button from "../components/Button.vue";

export default {
	name: "BookingEventCard",
	props: {
		price: String,
	},
	components: {
		Button,
	},
};
</script>

<style scoped>
.card p {
	color: #282142;
}

/* .btn-booking {
	background-color: #5465ff;
	color: #fff;
	padding: 12px 0;
	border-radius: 10px;
	border: none;
	box-shadow: 0 1px 2px rgba(0, 0, 0, 0.15);
	transition: box-shadow 0.3s ease-in-out;
}

.btn-booking:hover {
	background-color: #3a49ca;
	box-shadow: 0 5px 15px rgba(0, 0, 0, 0.3);
} */

.card h5 {
	font-size: 0.8rem;
	color: #8981a8;
	line-height: 1.5;
}
</style>
