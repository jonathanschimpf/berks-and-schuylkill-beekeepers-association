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

		const script = document.createElement('script');
		script.src = 'https://connect.facebook.net/en_US/sdk.js#xfbml=1&version=v19.0';
		script.async = true;
		script.defer = true;
		script.crossOrigin = 'anonymous';
		script.onload = () => {
			if (window.FB) {
				FB.init({
					xfbml: true,
					version: 'v19.0'
				});
				FB.XFBML.parse();
			}
			fbLoaded = true;
		};
		document.body.appendChild(script);
	});
</script>

<div class="topcenteringcontainer" in:fade={{ duration: 2000 }}>
	<div class="heading-container">
		<a
			href="https://www.facebook.com/BerksSchuylkillBeekeepers"
			rel="noreferrer"
			target="_blank"
			aria-label="Berks Schuylkill Beekeepers Association"
			class="no-text-decoration heading-link"
		>
			<h2>Connect</h2>
		</a>
		<a
			href="https://www.facebook.com/BerksSchuylkillBeekeepers"
			rel="noreferrer"
			target="_blank"
			aria-label="Berks Schuylkill Beekeepers Association"
			class="icon-link"
		>
			<FontAwesomeIcon icon={faFacebook} class="fa-2xl" style="color: #4267B2;" />
		</a>
	</div>

	<a
		href="https://www.facebook.com/BerksSchuylkillBeekeepers"
		rel="noreferrer"
		target="_blank"
		aria-label="Beekeepers Connecting"
	>
		<img
			src={`/images/douglas-raggio-vZGvVTO1pIg-unsplash.jpg`}
			class="beekeepersconnectingphoto"
			alt="Beekeepers Connecting"
		/>
	</a>
</div>

{#if !fbLoaded}
	<div class="loading-container" in:fade={{ duration: 2500 }}>
		<p class="loading-facebook-msg">Loading Facebook...</p>
	</div>
{:else}
	<!-- Facebook PLUG-IN -->
	<div class="facebook-plugin-container" in:fade={{ duration: 3000 }}>
		<div
			class="fb-page"
			data-href="https://www.facebook.com/BerksSchuylkillBeekeepers"
			data-tabs="timeline"
			data-small-header="false"
			data-adapt-container-width="true"
			data-hide-cover="false"
			data-show-facepile="true"
			data-height="5000"
		></div>
	</div>
{/if}

<style>
	.heading-container {
		display: flex;
		align-items: center;
	}

	.heading-link {
		display: flex;
		align-items: center;
	}

	.heading-link h2 {
		margin-right: 0.5rem;
	}

	.icon-link {
		display: flex;
		align-items: center;
		line-height: 1;
		margin-left: 7rem;
		padding-bottom: 0.80rem;
	}

	.topcenteringcontainer {
		display: flex;
		flex-direction: column;
		align-items: center;
		justify-content: center;
		margin-top: 8.5em;
	}

	.beekeepersconnectingphoto {
		width: 343px;
		border-radius: 5px;
		display: block;
	}
	.topcenteringcontainer a {
		text-decoration: none;
		color: inherit;
	}

	.loading-container {
		display: flex;
		justify-content: center;
		align-items: center;
		min-height: 10vh;
	}

	.loading-facebook-msg {
		color: #4267b2;
	}
	.facebook-plugin-container {
		display: flex;
		justify-content: center;
		align-items: center;
		max-width: 95vw;
		max-height: 95vh;
		margin: 0 auto;
		padding: 1em;
	}
	.fb-page {
		height: 80vh;
		border-radius: 5px;
	}
	h2 {
		color: rgb(0, 0, 0);
		font-weight: 900;
	}
</style>
