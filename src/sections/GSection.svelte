<script>
        import Dev from '../Assets/png-gralypho/Saly-11.png'
        import Carousel from '../Components/CarousselCards.svelte';

	    import { onMount } from "svelte";

	  onMount(() => {
    gsap.to(".dev", {
      scale: 1.3,
      ease: "bounce.out(1,0.3)",
      scrollTrigger: {
        trigger: ".dev",
        start: "top 600px",
	end: "-300px",
	scrub: 2,
      },
})
  });
</script>

<section class="G-section">
	<h1>Nos exemples de réalisations</h1>
	<h2>
		Selon vos besoins, nous utiliserons Wix, ou wordpress, ou sqarspace, Shopify, woo Commerce (...)
		ou n
	</h2>
        <img src={Dev} alt="icon de developpeur informatique" class="dev">
        <Carousel/>
	<div class="halo"></div>
</section>

<style>
	.G-section {
		display: grid;
		grid-template-columns: repeat(12, 1fr);
		grid-template-rows: auto;
		height: 100%;
		font-size: 16px;
		background-color: var(--colorO);
		margin-top: 170px;
	}
	.G-section h1 {
		grid-column: 2/6;
		grid-row: 1;
		font-family: epilogue;
		font-weight: bolder;
		font-size: 1.8em;
		color: white;
		text-transform: uppercase;
	}
	.G-section h2 {
		grid-column: 2/6;
		grid-row: 1;
		margin-top: 100px;
		font-family: epilogue;
		font-weight: 300;
		font-size: 1.2em;
		color: var(--colorC);
	}
        .dev{
                grid-column: 6/12;
                height: 150px;
                width: 150px;
                grid-row: 1;
                margin-left: 50px;
		z-index: 1;
		transform: scale(0.7);
        }
		.halo {
		grid-column: 7/12;
		grid-row: 1;
		background-color: rgb(79, 68, 235);
		width: 100px;
		height: 100px;
		border-radius: 50%;
		filter: blur(30px);
		z-index: 0;
		margin-left: 20px;
		margin-top: 0px;
	}

	@media screen and (max-width: 768px) {
		.G-section {
			font-size: 10px;
		}
	}
</style>
