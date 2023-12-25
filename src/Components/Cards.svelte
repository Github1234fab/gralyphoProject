<script>
	export let title;
	export let link;
	
</script>

<div class="card">
	<h2>{title}</h2>
	<a href={link} target="_blank"><button class="button">Voir</button></a>
</div>

<style>
	.card {
		position: relative;
		flex-shrink: 0;
		border-radius: 3px;
		border: none;
		margin: 8px;
		height: 20em;
		width: 20em;
		user-select: none;
		overflow: hidden;
		box-shadow:
			3px 5px 15px rgba(0, 0, 0, 0.573),
			-3px- 5px 15px rgba(0, 0, 0, 0.542);
		padding: 10px;
		background: radial-gradient(circle, var(--colorM) 2%, transparent);
	}
	.button {
		position: absolute;
		border-radius: 5px;
		font-family: DM sans;
		color: var(--colorC);
		font-size: 1em;
		top: 50%;
		left: 50%;
		width: 30%;
		transform: translate(-50%, -50%);
		padding: 10px;
		background-color: var(--colorA);
		border: none;
		cursor: pointer;
		box-shadow:
			2px 2px 5px black inset,
			-2px -2px 5px black inset;
	}
	.card h2 {
		font-family: kanit;
		font-size: 1.3em;
		font-weight: 200;
		padding: 20px;
		color: var(--colorC);
	}
	/* .card h3 {
		font-family: Kanit;
		font-weight: 500;
		padding: 20px;
		margin-top: -30px;
		color: white;
	}  */
</style>
