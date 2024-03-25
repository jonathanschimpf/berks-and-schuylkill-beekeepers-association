<script>
	import { base } from '$app/paths';
	import { page } from '$app/stores';

	// REACTIVE STATEMENT TO IDENTIFY THE CURRENT ROUTE AND SET THE APPROPRIATE ACTIVE CLASS
	$: activeRoute = $page.url.pathname;

	function closeNav() {
		let navbarCollapse = document.querySelector('.navbar-collapse');
		if (navbarCollapse.classList.contains('show')) {
			navbarCollapse.classList.remove('show');
		}
	}
</script>

<nav class="navbar navbar-expand-md navbar-light bg-transparent">
	<a class="navbar-brand" href="/">🐝</a>
	<button
		class="navbar-toggler"
		type="button"
		data-bs-toggle="collapse"
		data-bs-target="#navbarResponsive"
		aria-controls="navbarResponsive"
		aria-expanded="false"
		aria-label="Toggle navigation"
	>
		<span class="navbar-toggler-icon"></span>
	</button>

	<div class="collapse navbar-collapse justify-content-end" id="navbarResponsive">
		<ul class="navbar-nav">
			<li class="nav-item" class:active={activeRoute === `${base}/`}>
				<a on:click={closeNav} class="nav-link" href={`${base}/`}>Home</a>
			</li>
			<li class="nav-item" class:active={activeRoute === `${base}/aboutbeekeeping`}>
				<a on:click={closeNav} class="nav-link" href={`${base}/aboutbeekeeping`}>About</a>
			</li>
			<li class="nav-item" class:active={activeRoute === `${base}/connect`}>
				<a on:click={closeNav} class="nav-link" href={`${base}/connect`}>Connect</a>
			</li>
			<li class="nav-item" class:active={activeRoute === `${base}/contact`}>
				<a on:click={closeNav} class="nav-link" href={`${base}/contact`}>Contact</a>
			</li>
			<li class="nav-item" class:active={activeRoute === `${base}/dues`}>
				<a on:click={closeNav} class="nav-link" href={`${base}/dues`}>Dues</a>
			</li>
		</ul>
	</div>
</nav>

<style>
	.navbar-toggler {
		border: none;
		background-color: transparent;
		margin-right: 0.5em;
		outline-style: solid;
		outline-color: #e6cf00;
		outline-width: 3px;
	}

	.navbar-toggler-icon {
		background-image: url("data:image/svg+xml;charset=UTF-8,%3csvg viewBox='0 0 30 30' xmlns='http://www.w3.org/2000/svg'%3e%3cpath stroke='rgba(0, 0, 0, 1)' stroke-width='2' stroke-linecap='round' stroke-miterlimit='10' d='M4 7h22M4 15h22M4 23h22'/%3e%3c/svg%3e");
	}
	.navbar-brand {
		padding-left: 1rem;
	}

	@media (max-width: 767px) {
		.navbar-nav {
			flex-direction: column;
			width: 100%;
		}

		.navbar-collapse {
			background-color: transparent;
		}
	}
	@media (max-width: 767px) {
		.navbar {
			position: relative;
		}

		.navbar-nav {
			position: absolute;
			top: 80%; /*HEADROOM FOR THE VERTICAL COLUMN DROP-DOWN NAV*/
			right: 0;
			flex-direction: column;
			width: auto;
			background-color: transparent;
			border-bottom: none;
			box-shadow: none;
			margin-right: 0.2em;
			padding-top: 8px;
		}
	}

	.navbar-nav .nav-item {
		width: 100%;
	}

	.nav-item.active .nav-link {
		text-decoration: underline;
		text-decoration-color: #e6cf00;
		text-decoration-thickness: 3px; /* UNDERLINE THICKNESS */
		text-underline-offset: 3px; /* SPACE BETWEEN TEXT & UNDERLINE */
	}
	.nav-link {
		padding-bottom: 0;
		padding-top: 4px;
	}
</style>