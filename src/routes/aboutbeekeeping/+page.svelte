<script>
	import { base } from '$app/paths';
</script>

<div src=${base} class="maincenteringcontainer " >

    <h2>About Beekeeping</h2>
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
</style>