<template>
	<div class="banner w-100">
		<div class="container">
			<div class="row">
				<div class="col">
					<div class="headline w-50 my-auto text-center text-white">
						<h1 class="fw-bold">{{ headline }}</h1>
					</div>
				</div>
			</div>
		</div>
	</div>
</template>

<script>
export default {
	data() {
		return {
			headline: "Life is short! go find a new experience!",
			subHeadline:
				"Lorem ipsum dolor sit amet consectetur adipisicing elitNemo expedita dignissimos quis veritatis. Et ipsa quas delectus saepe mollitia nemo minima commodi, magni, quia provident, laboriosam tempora illum officia natus",
			imgUrl:
				"https://images.unsplash.com/photo-1493225457124-a3eb161ffa5f?ixlib=rb-1.2.1&ixid=MnwxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8&auto=format&fit=crop&w=870&q=80",
		};
	},
};
</script>

<style>
/* .banner {
	background-image: url("https://images.unsplash.com/photo-1493225457124-a3eb161ffa5f?ixlib=rb-1.2.1&ixid=MnwxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8&auto=format&fit=crop&w=870&q=80");
	height: 700px;
	background-repeat: no-repeat;
	background-position: center;
	background-size: cover;
} */
.banner {
	background-image: url("https://images.unsplash.com/photo-1487954152950-e0584673b7f3?ixlib=rb-1.2.1&ixid=MnwxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8&auto=format&fit=crop&w=870&q=80");
	height: 700px;
	background-repeat: no-repeat;
	background-position: center;
	background-size: cover;
	position: relative;
}

.headline {
	position: absolute;
	top: 50%;
	left: 50%;
	transform: translate(-50%, -50%);
}
</style>
