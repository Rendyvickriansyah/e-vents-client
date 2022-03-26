<template>
	<div class="container">
		<div class="row">
			<div class="col text-white">
				<h1>
					{{ event.title }}
				</h1>
				<p>
					{{ event.description }}
				</p>
			</div>
		</div>
	</div>
</template>

<script>
export default {
	props: ["id"],
	data() {
		return {
			event: "",
		};
	},
	mounted() {
		fetch(`http://localhost:1337/api/events/${this.id}`)
			.then((res) => res.json())
			.then((data) => (this.event = data.data.attributes))
			.catch((err) => console.log(err));
	},
};
</script>

<style></style>
