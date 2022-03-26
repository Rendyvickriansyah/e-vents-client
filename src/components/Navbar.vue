<template>
	<nav class="navbar navbar-expand-lg navbar-light bg-white">
		<div class="container">
			<a class="navbar-brand d-flex align-items-center" href="#"
				><i class="ri-coupon-3-fill ri-lg me-2"></i>Ngivent Kuy</a
			>
			<button
				class="navbar-toggler"
				type="button"
				data-bs-toggle="collapse"
				data-bs-target="#navbarSupportedContent"
				aria-controls="navbarSupportedContent"
				aria-expanded="false"
				aria-label="Toggle navigation"
			>
				<span class="navbar-toggler-icon"></span>
			</button>
			<div class="collapse navbar-collapse" id="navbarSupportedContent">
				<ul class="navbar-nav ms-auto mb-2 mb-lg-0">
					<li>
						<a class="nav-link me-2" aria-current="page" href="#">Sign up</a>
					</li>
					<li>
						<a class="nav-link button" aria-current="page" href="#">Login</a>
					</li>
				</ul>
			</div>
		</div>
	</nav>
</template>

<script>
export default {
	name: "Navbar",
};
</script>

<style scoped>
.button {
	background-color: #5465ff;
	color: #ffffff !important;
	padding: 12px 32px !important;
	border-radius: 12px;
	text-align: center;
	text-decoration: none;
	display: inline-block;
	font-size: 16px;
	cursor: pointer;
}

.navbar-brand i {
	color: #5465ff;
}

.navbar-brand {
	font-size: 1.5rem;
	font-weight: bold;
}

/* textarea:focus,
input[type="text"]:focus,
input[type="password"]:focus,
input[type="datetime"]:focus,
input[type="datetime-local"]:focus,
input[type="date"]:focus,
input[type="month"]:focus,
input[type="time"]:focus,
input[type="week"]:focus,
input[type="number"]:focus,
input[type="email"]:focus,
input[type="url"]:focus,
input[type="search"]:focus,
input[type="tel"]:focus,
input[type="color"]:focus,
.uneditable-input:focus {
	border-color: #fff;
	box-shadow: 0 0 0 2px rgba(255, 255, 255, 0.3);
	outline: 0 none;
	color: #fff;
}
textarea,
input[type="text"],
input[type="password"],
input[type="datetime"],
input[type="datetime-local"],
input[type="date"],
input[type="month"],
input[type="time"],
input[type="week"],
input[type="number"],
input[type="email"],
input[type="url"],
input[type="search"],
input[type="tel"],
input[type="color"],
.uneditable-input {
	outline: 0 none;
	background: #322f49;
} */
</style>
