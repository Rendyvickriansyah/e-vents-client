<template>
	<div class="container py-5">
		<div class="row">
			<div class="col">
				<h4>Events</h4>
				<div class="d-flex my-5">
					<div v-for="(event, index) in events.data" :key="index" class="me-3">
						<div class="card border-0">
							<!-- <img
								:src="
									require(`../../../e-vents-api/public${event.attributes.cover.data.attributes.formats.thumbnail.url}`)
								"
							/> -->
							<img
								:src="
									require(`../../../e-vents-api/public${event.attributes.cover.data.attributes.formats.thumbnail.url}`)
								"
							/>
							<div class="card-body">
								<p class="card-text">{{ event.attributes.duration }} Hours</p>
								<h5 class="card-title text-white">
									{{ event.attributes.title }}
								</h5>
								<p class="card-text">{{ event.attributes.date }}</p>

								<router-link
									:to="{ name: 'eventDetail', params: { id: event.id } }"
									class="btn btn-sm rounded btn-primary mt-3"
								>
									View Events
								</router-link>
							</div>
						</div>
					</div>
				</div>
			</div>
		</div>
	</div>
</template>

<script>
import axios from "axios";
import { onMounted, ref } from "vue";

export default {
	name: "Cards",
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
};
</script>

<style>
.card {
	max-width: 16rem;
	border-radius: 20px !important;
	background-color: #252836 !important;
}

.thumb {
	border-radius: 20px !important;
}

.card-body h5 {
	line-height: 1.5;
}

.card-body p {
	color: #8e90aa;
	font-size: 0.8rem;
}
</style>
