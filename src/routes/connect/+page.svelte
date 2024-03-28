<script>
	import { onMount } from 'svelte';
	import { FontAwesomeIcon } from '@fortawesome/svelte-fontawesome';
	import { faFacebook } from '@fortawesome/free-brands-svg-icons';
	import { fade } from 'svelte/transition';
  </script>
  
  <div class="all-connect-items-centered">
	<div class="topcenteringcontainer">
	  <div class="heading-container">
		<a
		  href="https://www.facebook.com/BerksSchuylkillBeekeepers"
		  rel="noreferrer"
		  target="_blank"
		  aria-label="Berks Schuylkill Beekeepers Association"
		  class="heading-link"
		>
		  <h2 class="no-underline">Connect</h2>
		</a>
		<a
		  href="https://www.facebook.com/BerksSchuylkillBeekeepers"
		  rel="noreferrer"
		  target="_blank"
		  aria-label="Facebook Page"
		  class="icon-link"
		>
		  <FontAwesomeIcon icon={faFacebook} class="fa-2xl" style="color: #4267B2; margin-bottom: 10px;" />
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
  
	<div class="facebook-plugin-container" in:fade={{ duration: 3000 }}>
	  <iframe
		src="https://www.facebook.com/plugins/page.php?href=https%3A%2F%2Fwww.facebook.com%2FBerksSchuylkillBeekeepers&tabs=timeline&width=350&height=2500&small_header=false&adapt_container_width=true&hide_cover=false&show_facepile=true&appId"
		width="350"
		height="2500"
		style="border:none;overflow:hidden"
		scrolling="no"
		frameborder="0"
		allowfullscreen="true"
		allow="autoplay; clipboard-write; encrypted-media; picture-in-picture; web-share"
		title="Facebook Social Plugin"
	  ></iframe>
	</div>
  </div>
  
  <style>
	.all-connect-items-centered {
	  display: flex;
	  flex-direction: column;
	  align-items: center;
	  justify-content: center;
	  margin-top: 80px;
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
  
	.no-underline {
	  text-decoration: none;
	  margin-right: 5.5rem;
	  color: black;
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
	  width: 100%;
	  max-width: 350px;
	  border-radius: 5px;
	}
  
	.facebook-plugin-container {
	  display: flex;
	  justify-content: center;
	  align-items: center;
	  width: 100%;
	  max-width: 350px;
	  margin-top: 1em;
	}
  </style>
  