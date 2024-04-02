<script>
	import { FontAwesomeIcon } from '@fortawesome/svelte-fontawesome';
	import { faFacebook } from '@fortawesome/free-brands-svg-icons';
	import { fade } from 'svelte/transition';
</script>

<div class="maincenteringcontainer">
	<div class="topcenteringcontainer" in:fade={{ duration: 150 }}>
		<div class="heading-container" in:fade={{ duration: 150 }}>
			<a
				href="https://www.facebook.com/BerksSchuylkillBeekeepers"
				rel="noreferrer"
				target="_blank"
				aria-label="Berks Schuylkill Beekeepers Association"
				class="heading-link"
			>
				<h2 class="h2connect no-underline">Connect</h2>
			</a>
			<a
				href="https://www.facebook.com/BerksSchuylkillBeekeepers"
				rel="noreferrer"
				target="_blank"
				aria-label="Facebook Page"
				class="icon-link"
			>
				<FontAwesomeIcon
					icon={faFacebook}
					class="fa-2xl"
					style="color: #4267B2; margin-bottom: 10px;"
				/>
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
	<div in:fade={{ duration: 1500 }}>
		<iframe
			title="Berks and Schuylkill
Beekeepers Association — We'll help anyone who wants to raise bees."
			src="https://www.facebook.com/plugins/page.php?href=https%3A%2F%2Fwww.facebook.com%2FBerksSchuylkillBeekeepers&tabs=timeline&width=415&height=5000&small_header=false&adapt_container_width=true&hide_cover=false&show_facepile=true&appId"
			width="415"
			height="2630"
			style="border:none;overflow:hidden"
			scrolling="no"
			frameborder="0"
			allowfullscreen="true"
			allow="autoplay; clipboard-write; encrypted-media; picture-in-picture; web-share"
		></iframe>
	</div>

	<a
		href="https://www.facebook.com/BerksSchuylkillBeekeepers"
		rel="noreferrer"
		target="_blank"
		aria-label="Facebook Page"
		class="facebook-link-below
		no-underline"
	>
	</a>
</div>

<style>
	.maincenteringcontainer {
		display: flex; /* [CRUCIAL] ESTABLISHES THE CONTAINER AS A FLEX CONTAINER */
		flex-direction: column; /* STACKS THE CHILDREN VERTICALLY */
		align-items: center; /* CENTERS CHILDREN ALONG THE HORIZONTAL CROSS ACCESS */
		justify-content: center; /* CENTERS CHILDREN ACROSS THE MAIN VERTICAL AXIS */
		margin-top: 11em;
	}

	.heading-container {
		display: flex;
		align-items: center;
	}

	.heading-link {
		display: flex;
		align-items: center;
		text-decoration: none;
	}

	h2.no-underline {
		text-decoration: none;
		color: black;
	}

	h2 {
		margin-right: 100px;
	}

	.h2connect:hover {
		color: #4267b2;
	}

	.facebook-link-below {
		display: flex;
		align-items: center;
		text-decoration: none;
	}

	.icon-link {
		display: flex;
		align-items: center;
		line-height: 1;
		margin-left: 1rem;
	}

	.topcenteringcontainer {
		display: flex;
		flex-direction: column;
		align-items: center;
		justify-content: center;
		margin-top: 2em;
	}

	.beekeepersconnectingphoto {
		width: 415px;
		border-radius: 5px;
		margin-bottom: 20px;
	}
</style>
