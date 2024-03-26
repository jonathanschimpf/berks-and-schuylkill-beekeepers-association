<script>
	// NAV COMPONENT IMPORT
	import Nav from '$lib/Nav.svelte';
  
	// BOOTSTRAP CSS IMPORT
	import 'bootstrap/dist/css/bootstrap.min.css';
  
	// VITE'S WAY OF HANDLING STATIC ASSETS
	import bootstrapBundle from 'bootstrap/dist/js/bootstrap.bundle.min.js?url';
  </script>
  
  <svelte:head>
	<!-- BOOTSTRAP'S JS BUNDLE SO IT WILL BE SERVED SERVER SIDE -->
	<script src="{bootstrapBundle}" defer></script>
  </svelte:head>
  
  <!-- NAV AND SLOT FOR PAGE CONTENT -->
  <Nav />
  <slot />
  
  <style>
	:global(body, html) {
	  background-color: rgb(255, 255, 255) !important; /* SPECIFIC OVERRIDE */
	  font-family: 'Futura', sans-serif; 
	}
  </style>
  