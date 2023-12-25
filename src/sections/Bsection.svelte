<script>
        import Customers from '../Components/Customers.svelte';

</script>
<section class="B-section">
<Customers/>

</section>
<style>
        	.B-section {
		display: grid;
		grid-template-columns: repeat(12, 1fr);
		grid-template-rows: auto;
		height: 100%;
		margin: 0 0px;
		font-size: 16px;
		background-color: var(--colorO);
		overflow: hidden;
	}
	@media screen and (max-width: 768px) {
		.B-section {
			font-size: 10px;
		}
	}
        
</style>