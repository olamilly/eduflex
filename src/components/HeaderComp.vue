<template>
	<nav class="navbar navbar-expand-sm">
		<div class="container-fluid">
			<div class="brand px-3 d-flex justify-content-center align-items-center">
				<img src="/Logo.svg" /><span class="ms-1">EduFlex</span>
			</div>
			<button
				class="navbar-toggler"
				type="button"
				data-bs-toggle="collapse"
				data-bs-target="#navbar"
				aria-controls="navbar"
				aria-expanded="false"
				aria-label="Toggle navigation"
			>
				<span class="navbar-toggler-icon"></span>
			</button>

			<div class="collapse navbar-collapse" id="navbar">
				<ul class="navbar-nav mb-sm-0">
					<li class="nav-item">
						<a class="nav-link text-center" aria-current="page" href="#"
							>Home</a
						>
					</li>
					<li class="nav-item">
						<a class="nav-link text-center" href="#">Courses</a>
					</li>
					<li class="nav-item">
						<a class="nav-link text-center" href="#">Community</a>
					</li>
					<li class="nav-item">
						<a class="nav-link text-center" href="#">About</a>
					</li>
					<li class="nav-item last">
						<a class="nav-link text-center fw-bolder" href="#">Sign in</a>
					</li>
				</ul>
			</div>
		</div>
	</nav>
</template>
<style scoped>
	.nav-item {
		padding: 0.8rem;
		padding-left: 1.3rem;
		padding-right: 1.3rem;
	}

	.nav-item > a {
		font-size: 13px;
	}
	.navbar,
	.navbar > .container-fluid {
		padding: 0px !important;
		background-color: #f9f5f2;
		border-bottom: 0.7px solid black;
	}
	.navbar > .container-fluid {
		min-height: 60px;
		align-items: stretch;
	}
	.collapse {
		align-items: stretch;
	}
	.nav-link:hover {
		font-weight: bolder !important;
	}
	@media (max-width: 575px) {
		.nav-item {
			border-bottom: 0.7px solid black;
		}
	}
	@media (min-width: 576px) {
		.navbar-expand-sm .navbar-collapse {
			justify-content: flex-end !important;
		}
		.brand {
			background-color: #ecebff;
			border-right: 0.5px solid black;
		}
		.nav-item {
			border-left: 1px solid black;
		}
	}

	.brand > span {
		font-weight: 700;
		font-size: 16px;
	}
	.nav-item.last {
		background-color: #f2c161;
	}
	.navbar-toggler {
		border: none;
	}
	.navbar-toggler:focus {
		box-shadow: none;
	}
</style>
