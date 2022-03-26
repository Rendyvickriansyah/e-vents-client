<template>
	<div class="footer py-5">
		<div class="container">
			<div class="row text-white">
				<div class="col col-lg-4">
					<div class="navbar-brand d-flex align-items-center mb-4" href="#">
						<i class="ri-coupon-3-fill ri-lg me-2"></i>Ngivent Kuy
					</div>
					<p>
						{{ brand }}
					</p>
					<p>
						{{ office }}
					</p>
				</div>
				<div class="col">
					<h5 class="mb-4">Terms & Policies</h5>
					<div v-for="term in termsPolicies" :key="term.id">
						<p>{{ term.title }}</p>
					</div>
				</div>
				<div class="col">
					<h5 class="mb-4">Company</h5>
					<div v-for="company in companys" :key="company.id">
						<p>{{ company.title }}</p>
					</div>
				</div>
				<div class="col">
					<h5 class="mb-4">Social</h5>
					<div v-for="social in socials" :key="social.id">
						<p>{{ social.title }}</p>
					</div>
				</div>
			</div>
		</div>
	</div>
</template>

<script>
export default {
	name: "Footer",
	data() {
		return {
			logo: "",
			brand: "Ngivent Kuy © 2022",
			office:
				"Prudential Center Lantai 22, Mall Kota Kasablanka, Jl. Casablanca Raya Kav. 88 Jakarta Selatan 12950",
			termsPolicies: [
				{
					id: 1,
					title: "Terms & Policies",
				},
				{
					id: 2,
					title: "Privacy Policy",
				},
				{
					id: 3,
					title: "Cookie Policy",
				},
				{
					id: 4,
					title: "GDPR",
				},
				{
					id: 5,
					title: "Sitemap",
				},
			],
			companys: [
				{
					id: 1,
					title: "FAQ",
				},
				{
					id: 2,
					title: "Contact Us",
				},
				{
					id: 3,
					title: "Careers",
				},
				{
					id: 4,
					title: "About Us",
				},
				{
					id: 5,
					title: "Blog",
				},
			],
			socials: [
				{
					id: 1,
					title: "Facebook",
				},
				{
					id: 2,
					title: "Twitter",
				},
				{
					id: 3,
					title: "Instagram",
				},
				{
					id: 4,
					title: "Youtube",
				},
				{
					id: 5,
					title: "Linkedin",
				},
			],
		};
	},
};
</script>

<style>
.navbar-brand i {
	color: #5465ff;
}
.footer {
	background-color: #0b0434;
}

.footer p {
	color: #c5c5c5;
	font-size: 1rem;
}
</style>
