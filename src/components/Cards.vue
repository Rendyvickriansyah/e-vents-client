<template>
	<div class="container py-5">
		<div class="row">
			<div class="col">
				<img src="" alt="" />
			</div>
		</div>
		<div class="row">
			<div class="col">
				<h4>Upcoming Events</h4>
			</div>
		</div>
		<div class="row row-cols-1 row-cols-md-3 g-3 mt-4">
			<div v-for="(event, index) in events.data" :key="index" class="">
				<router-link
					:to="{ name: 'eventDetail', params: { id: event.id } }"
					class="text-decoration-none"
				>
					<div class="col">
						<div class="card border-0 h-100">
							<div class="card-header border-0 bg-transparent">
								<img
									:src="
										require(`../../../e-vents-api/public${event.attributes.cover.data.attributes.formats.medium.url}`)
									"
									class="h-75 card-img-top"
									alt="#"
								/>
								<span class="badge bg-light text-dark">{{
									event.attributes.price
								}}</span>
							</div>

							<div class="card-body">
								<p>
									<i class="ri-calendar-2-line me-2"></i>
									{{
										event.attributes.date && event.attributes.date.length <= 10
											? event.attributes.date
											: event.attributes.date.substring(0, 10) + ""
									}}
								</p>
								<h5 class="card-title">{{ event.attributes.title }}</h5>
								<p class="card-text mt-3">
									<i class="ri-map-pin-2-line"></i>
									{{
										event.attributes.location &&
										event.attributes.location.length <= 65
											? event.attributes.location
											: event.attributes.location.substring(0, 65) + "..."
									}}
								</p>
							</div>
						</div>
					</div>
				</router-link>
			</div>
		</div>
	</div>
</template>

<script>
import axios from "axios";
import { onMounted, ref } from "vue";

export default {
	name: "Cards",
	// data() {
	// 	return {
	// 		search: "",
	// 	};
	// },
	setup() {
		let events = ref([]);
		onMounted(() => {
			// Get data from api endpoint
			axios
				.get("http://localhost:1337/api/events?populate=*")
				.then((result) => {
					events.value = result.data;
				})
				.catch((err) => {
					console.log(err.response);
				});
		});
		return {
			events,
		};
	},
	// computed: {
	// 	filteredData() {
	// 		return this.events.filter((entry) =>
	// 			this.events.length
	// 				? Object.keys(this.events[0]).some((key) =>
	// 						("" + entry[key]).toLowerCase().includes(this.search)
	// 				  )
	// 				: true
	// 		);
	// 	},
	// },
};
</script>

<style>
.card-header img {
	position: relative;
}

.card-header span {
	position: absolute;
	top: 5%;
	left: 10%;
	z-index: 3;
}

.card-body h5 {
	color: #282142;
}

.card-body p {
	font-size: 0.8rem;
	color: #686087;
	line-height: 1.5;
}

.card {
	/* max-width: 16rem; */
	border-radius: 20px !important;
	background-color: #ffffff !important;
}
.card img {
	border-radius: 20px !important;
}

.card-body h5 {
	line-height: 1.5;
	margin-top: -12px;
}

.card-body p {
	font-size: 0.8rem;
}
</style>
