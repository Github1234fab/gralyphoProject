<script>
	export let title;
	export let p;
	export let img;
	export let alt;
	export let job;
</script>

<div class="wrapper-cards">
	<div class="card">
		<img src={img} {alt} class="img" />
		<h3>{title}</h3>
		<h4>{job}</h4>
		<h5>{p}</h5>
	</div>
</div>

<style>
	.wrapper-cards {
		display: flex;
		grid-column: 3/9;
		grid-row: 3;
	}
	.card {
		display: flex;
		flex-direction: column;
		justify-content: center;
		align-items: center;
		gap: 15px;
		width: 100%;
		height: 400px;
		font-family: epilogue;
		background-color: rgba(6, 6, 70, 0.271);
		    box-shadow: 3px 3px 5px rgb(1, 6, 27);
		padding: 20px;
	}
	.card h3 {
		font-size: 1.4em;
		color: var(--colorC);
		font-weight: 700;
	}
	.card h5 {
		font-size: 1em;
		color: var(--colorC);
		font-weight: 100;
		text-align: center;
	}
	.img {
		width: 100px;
		height: 100px;
		object-fit: cover;
	}
	.card h4 {
		font-size: 1.2em;
		color: white;
	}

</style>
