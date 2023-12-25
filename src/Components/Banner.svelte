<script>
	import { onMount } from 'svelte';

onMount(() => {


    const timeline = gsap.timeline();

    // Utilisez le sélecteur de classe directement
    timeline.to(".banner-icon", {
      opacity: 1,
      y: 0,
       stagger: 0.2, 
      duration: 0.5,
      scrollTrigger: {
        trigger: ".banner-icon", // Utilisez le sélecteur de classe ici aussi
        start: "top 600px",
	end: "-300px",
	scrub: 2,
      },
    });
  });


</script>

<div class="cont">
  <div class="banner-wrapper">
    <i class="fa-solid fa-desktop banner-icon"><span>Sites Web</span><i class="fa-solid fa-arrow-right arrow" /></i>
    <i class="fa-solid fa-magnifying-glass-chart banner-icon"
      ><span>Applications</span><i class="fa-solid fa-arrow-right arrow" /></i
    >
    <i class="fa-solid fa-magnifying-glass-chart banner-icon"
      ><span>Référencement</span><i class="fa-solid fa-arrow-right arrow" /></i
    >
    <i class="fa-solid fa-comments-dollar banner-icon"
      ><span>Marketing</span><i class="fa-solid fa-arrow-right arrow" /></i
    >
    <i class="fa-solid fa-comments-dollar banner-icon"
      ><span>Composants</span><i class="fa-solid fa-arrow-right arrow" /></i
    >
    <i class="fa-solid fa-wand-magic-sparkles banner-icon"
      ><span>Refonte</span><i class="fa-solid fa-arrow-right arrow" /></i
    >
  </div>
</div>

<style>
  .cont {
    background-color: transparent;
    grid-column: 2/11;
    grid-row: 2;
  }
  .banner-wrapper {
    display: flex;
    flex-direction: row;
    flex-wrap: wrap;
    gap: 30px;
    align-items: center;
    justify-content: center;
    margin-top: 100px;
  }
  .banner-icon {
    opacity: 0.3;
    background-color: transparent;
    font-size: 1.5em;
    color: var(--colorD);
    display: flex;
    flex-direction: column;
    padding: 10px;
    gap: 20px;
    align-items: center;
    width: 6em;
    height: 6em;
    border-radius: 5%;
    justify-content: center;
    transition: 0.3s ease-in-out;
    box-shadow:
      2px 2px 15px rgba(15, 15, 15, 0.606),
      -2px -2px 15px rgba(16, 16, 16, 0.599);
  }

  .banner-icon span {
    font-size: 0.6em;
    font-family: kanit;
    font-weight: 500;
    color: var(--colorC);
    letter-spacing: -0.04em;
  }
  /* .banner-icon:hover {
		transform: scale(1);
		background-color: var(--colorL);
	} */
  .arrow {
    cursor: pointer;
    transition: 0.2s ease-in-out;
    color: var(--colorA);
  }
  .arrow:hover {
    transform: scale(1.2);
  }

  /* @media screen and (min-width: 998px) {
		.banner-wrapper {
			grid-template-columns: repeat(2, 1fr);
		}
		.banner-icon {
			background-color: transparent;
			font-size: 1.6em;
			width: 25em;
			height: 12em;
		}
		.banner-icon span {
			font-size: 1.4em;
			font-family: kanit;
			font-weight: 500;
			color: var(--colorC);
			letter-spacing: -0.04em;
		}
		.arrow {
		font-size: 1.8em;
	}
	}
	@media screen and (max-width: 768px){
		.banner-wrapper {
			grid-template-columns: repeat(1, 1fr);
		}
		.banner-icon {
			background-color: transparent;
			font-size: 1.6em;
			width: 100%;
			height: 12em;
		}
		.banner-icon span {
			font-size: 1em;
			font-family: kanit;
			font-weight: 500;
			color: var(--colorC);
			letter-spacing: -0.04em;
		}
		.arrow {
		font-size: 1.8em;
	}
} */
</style>
