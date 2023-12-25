<script>
import Climber from '../Assets/png-gralypho/Saly-15.png';

    import { onMount } from "svelte";

	  onMount(() => {
    gsap.to(".climb", {
rotate: 360,
      scale: 1,
      scrollTrigger: {
        trigger: ".climb",
        start: "top 600px",
	end: "-300px",
	scrub: 2,
      },
})
  });

</script>

<section class="H-section">

        <h1>Les meilleurs c’est nous</h1>
        <h2>Selon vos besoins, nous utiliserons Wix, ou wordpress, ou sqarspace, Shopify, woo Commerce (...) ou n</h2>
        <img src={Climber} alt="" class="climb">
	<div class="halo"></div>

</section>


<style>
.H-section {
		display: grid;
		grid-template-columns: repeat(12, 1fr);
		grid-template-rows: auto;
		height: 100%;
		font-size: 16px;
		background-color: var(--colorO);
		margin-top: 150px;
	}
	.H-section h1 {
		grid-column: 4/12;
		grid-row: 1;
		font-family: epilogue;
		font-weight: bolder;
		font-size: 1.8em;
		color: white;
		text-transform: uppercase;
	}
	.H-section h2 {
		grid-column: 4/12;
		grid-row: 1;
		margin-top: 100px;
		font-family: epilogue;
		font-weight: 300;
		font-size: 1.2em;
		color: var(--colorC);
	}
        .climb{
                grid-column: 2/3;
                height: 160px;
                width: 100px;
                grid-row: 1;
                margin-top: -30px;
		z-index: 1;
                
        }
		.halo {
		grid-column: 2/3;
		grid-row: 1;
		background-color: rgb(79, 68, 235);
		width: 80px;
		height: 80px;
		border-radius: 50%;
		filter: blur(30px);
		z-index: 0;
		margin-left: 20px;
		margin-top: 20px;
	}
        	@media screen and (max-width: 768px) {
		.H-section {
			font-size: 10px;
		}
	}

</style>