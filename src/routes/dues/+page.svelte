<script>
	import { faPaypal } from '@fortawesome/free-brands-svg-icons';
	import { FontAwesomeIcon } from '@fortawesome/svelte-fontawesome';
</script>

<div class="maincenteringcontainer">
	<a
		href="https://www.paypal.com/paypalme/BSCBeekeepers"
		target="_blank"
		class="paypal-link"
		aria-label="PayPal - Berks Schuylkill Beekeepers Association"
	>
		<FontAwesomeIcon
			icon={faPaypal}
			size="3x"
			style="color: #253b7d; margin-bottom: 1rem; display: block;"
		/>
	</a>
	<a
		href="https://www.paypal.com/paypalme/BSCBeekeepers"
		target="_blank"
		class="btn btn-lg btn-warning duesbutton"
		role="button"
	>
		Pay Dues with PayPal
	</a>
</div>

<style>
	.maincenteringcontainer {
		text-align: center;
		display: flex; /* [CRUCIAL] ESTABLISHES THE CONTAINER AS A FLEX CONTAINER */
		flex-direction: column; /* STACKS THE CHILDREN VERTICALLY */
		align-items: center; /* CENTERS CHILDREN ALONG THE HORIZONTAL CROSS ACCESS */
		justify-content: center; /* CENTERS CHILDREN ACROSS THE MAIN VERTICAL AXIS */
		margin-top: 10em;
	}

	.paypal-link {
		display: inline-block;
		margin-bottom: 1rem;
		text-decoration: none;
	}
	.duesbutton {
		background-color: #f0d800;
		color: rgb(116, 116, 116);
		outline-style: solid;
		outline-color: #f0d800;
		outline-width: 5px;
		border: 1px solid transparent;
		transition:
			background-color 0.2s,
			color 0.2s; /* SMOOTH TRANSITION BBECAUSE */
	}

	.duesbutton:hover,
	.duesbutton:active {
		/* ACTIVE STATE THAT RESEMBLES THE HOVER ON A DESKTOP 
		TO CONFIRM THE BUTTON WAS PRESSED */
		background-color: white;
		color: #a49400;
		outline-style: solid;
		outline-color: #f0d800;
		outline-width: 5px;
	}

	/* RESETS TO MATCH THE DEFAULT STATE */
	@media (hover: none) {
		.duesbutton:hover {
			background-color: #f0d800; 
			color: rgb(116, 116, 116); 
		}
		.duesbutton:active {
			background-color: white; 
			color: #a49400; 
		}
	}
</style>
