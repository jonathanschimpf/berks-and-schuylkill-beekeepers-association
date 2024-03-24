<script>
	import 'bootstrap/dist/css/bootstrap.min.css';
	import Nav from '$lib/Nav.svelte';
</script>

<Nav />
<slot />

<style>
    	:global(body, html) {
		background-color: rgb(255, 255, 255) !important; /* SPECIFIC OVERRIDE */
		font-family: 'Futura', sans-serif; /* Futura OBVIOUSLY */
	}
</style>