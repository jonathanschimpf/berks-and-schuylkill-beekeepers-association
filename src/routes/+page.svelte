<script>
	import { base } from '$app/paths';
</script>

<div src=${base} class="maincenteringcontainer">
	<h2>Berks and Schuylkill Beekeepers Association</h2>
	<p>We'll help anyone who wants to raise bees.</p>
</div>

<style>
	.maincenteringcontainer {
		display: flex; /* [CRUCIAL] ESTABLISHES THE CONTAINER AS A FLEX CONTAINER */
		flex-direction: column; /* STACKS THE CHILDREN VERTICALLY */
		align-items: center; /* CENTERS CHILDREN ALONG THE HORIZONTAL CROSS ACCESS */
		justify-content: center; /* CENTERS CHILDREN ACROSS THE MAIN VERTICAL AXIS */
		margin-top: 11em;
	}

	h2 {
		color: rgb(0, 0, 0);
        font-weight: 900;
	}

	@media (max-width: 767px) {
		h2 {
			font-size: 3.5vw;
		}
	}

	p {
		color: rgb(190, 190, 190);
	}

	@media (max-width: 767px) {
		p {
			font-size: 2vw;
		}
	}

</style>
