<script>
	// export let icon;
	export let title;
	export let p;
	export let number;
	import { onMount } from 'svelte';

	let isOpen = false;

	function toggleCollapse() {
		isOpen = !isOpen;
	}

	onMount(() => {
		const accordeonButton = document.getElementById('accordeonButton');
		const collapseExample = document.getElementById('collapseExample');

		accordeonButton.addEventListener('click', toggleCollapse);

		// Fermer le collapsible lorsque l'utilisateur clique en dehors de celui-ci
		document.addEventListener('click', (event) => {
			if (!accordeonButton.closest(event.target)) {
				isOpen = true;
			}
		});
	});
</script>

<div class="wrapper">
	<p class="d-inline-flex gap-1">
		<a
			id="accordeonButton"
			class="btn btn-primary accordeon"
			aria-expanded={isOpen ? 'true' : 'false'}
			aria-controls="collapseExample"
		>
			<span class="number"> {number} </span>
			<span>{title}</span>
		</a>
	</p>
	<div class="collapse" id="collapseExample" class:show={isOpen}>
		<div class="card text">
			{p}
		</div>
	</div>
</div>



<style>
	.show {
		display: block !important;
	}
	.wrapper {
		display: flex;
		flex-direction: column;
		/* background-color: var(--colorO); */
	}
	.accordeon {
		background-color: var(--colorO);
		padding: 10px;
		   box-shadow:
      2px 2px 15px rgba(15, 15, 15, 0.606),
      -2px -2px 15px rgba(16, 16, 16, 0.599);
		border-radius: 8px;
		border: none;
		width: 80vw;
		font-family: DM sans;
		display: flex;
		gap: 10px;
		color: var(--colorC);
		font-size: 1.1em;
		align-items: center;
	}
	.number {
		font-size: 1em;
		height: 20px;
		width: 20px;
		background-color: var(--colorD);
		border-radius: 50%;
		display: flex;
		align-items: center;
		justify-content: center;
		align-self: center;
		padding: 15px;
	}
	/* .text {
		padding: 20px;
		box-shadow:
			3px 3px 50px rgb(15, 15, 15),
			-3px -3px 50px rgb(16, 16, 16);
		border-radius: 8px;
		border: none;

		font-family: epilogue;
		display: flex;
		align-items: center;
		color: var(--colorA);
		font-weight: 100;
	} */
</style>
