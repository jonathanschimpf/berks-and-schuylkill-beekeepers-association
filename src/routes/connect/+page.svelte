<script>
	import { FontAwesomeIcon } from '@fortawesome/svelte-fontawesome';
	import { faFacebook } from '@fortawesome/free-brands-svg-icons';
	import { onMount } from 'svelte';
	import { fade } from 'svelte/transition';

	let fbLoaded = false;

	onMount(() => {
		let fbRoot = document.getElementById('fb-root');
		if (!fbRoot) {
			fbRoot = document.createElement('div');
			fbRoot.id = 'fb-root';
			document.body.insertBefore(fbRoot, document.body.firstChild);
		}

		if (!window.FB) {
			const script = document.createElement('script');
			script.src = 'https://connect.facebook.net/en_US/sdk.js#xfbml=1&version=v19.0';
			script.async = true;
			script.defer = true;
			script.crossOrigin = 'anonymous';
			script.onload = () => {
				FB.init({
					xfbml: true,
					version: 'v19.0'
				});
				FB.XFBML.parse();

				// Set fbLoaded to true once the SDK is initialized
				fbLoaded = true;
			};
			document.body.appendChild(script);
		} else {
			FB.XFBML.parse();
			// Set fbLoaded to true since the SDK was already loaded
			fbLoaded = true;
		}
	});
</script>

<div class="topcenteringcontainer" in:fade={{ duration: 2000 }} >
	<h2>
		Connect
		<a
			href="https://www.facebook.com/BerksSchuylkillBeekeepers"
			rel="noreferrer"
			target="_blank"
			aria-label="Nerks Schuylkill Beekeepers Association"
		>
			<FontAwesomeIcon icon={faFacebook} class="facebook-icon" />
		</a>
	</h2>
	<img
		src={`/images/douglas-raggio-vZGvVTO1pIg-unsplash.jpg`}
		class="beekeepersconnectingphoto"
		alt="Beekeepers Connecting"
	/>
</div>

{#if !fbLoaded}
	<div class="loading-container" in:fade={{ duration: 2500 }}>
		<FontAwesomeIcon icon={faFacebook} size="3x" />
		<p>Loading...</p>
	</div>
{/if}

<!-- Page plugin's code -->
<div class="facebook-plugin-container" in:fade={{ duration: 3000 }} >
	<div
		class="fb-page"
		data-href="https://www.facebook.com/BerksSchuylkillBeekeepers"
		data-tabs="timeline"
		data-small-header="false"
		data-adapt-container-width="true"
		data-hide-cover="false"
		data-show-facepile="true"
		data-height="1000"
	></div>
</div>

<style>
	.topcenteringcontainer {
		display: flex; /* [CRUCIAL] ESTABLISHES THE CONTAINER AS A FLEX CONTAINER */
		flex-direction: column; /* STACKS THE CHILDREN VERTICALLY */
		align-items: center; /* CENTERS CHILDREN ALONG THE HORIZONTAL CROSS ACCESS */
		justify-content: center; /* CENTERS CHILDREN ACROSS THE MAIN VERTICAL AXIS */
		margin-top: 8.5em;
	}
	.beekeepersconnectingphoto {
		width: 343px;
		border-radius: 5px;
	}
	:global(.facebook-icon) {
		color: #3b5998;
		margin-left: 0.5em;
		width: 32px !important;
		height: 32px !important;
	}
	.facebook-plugin-container {
		display: flex;
		justify-content: center; /* Centers horizontally in the flex container */
		align-items: center; /* Centers vertically in the flex container */
		max-width: 95vw;
		max-height: 95vh;
		margin: 0 auto; /* Centers the div itself horizontally if it's a block element */
		padding: 1em;
	}
	.fb-page {
		height: 80vh !important;
		border-radius: 5px !important;
	}

	h2 {
		color: rgb(0, 0, 0);
		font-weight: 900;
	}
</style>
