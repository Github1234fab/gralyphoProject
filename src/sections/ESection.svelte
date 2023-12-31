<script>
  import SpaceShip from "../Assets/png-gralypho/Saly-43.png";
  import Banner from "../Components/Banner.svelte";

  import { onMount } from "svelte";

  onMount(() => {
    gsap.to(".space-ship", {
      scale: 1.2,
      ease: "expoScale",
      scrollTrigger: {
        trigger: ".space-ship",
        start: "top 800px",
        end: "-200px",
        scrub: 1,
      },
    });
  });
</script>

<section class="E-section" id="sectionE">
  <div class="wrapper-text">
  <h1>Gralypho créer un service unique de produits numériques.</h1>
  <h2>Selon vos besoins, nous utiliserons Wix, ou wordpress, ou sqarspace, Shopify, woo Commerce (...).</h2>
  </div>
  <div class="wrapper-spaceShip">
    <img src={SpaceShip} alt="" class="space-ship" />
  </div>
</section>

<Banner />

<style>
  .E-section {
    scroll-margin-top: 90px;
    display: grid;
    grid-template-columns: repeat(12, 1fr);
    grid-template-rows: auto;
    margin-top: 150px;
    height: 100%;
    font-size: 16px;
    background-color: var(--colorO);
  }
  .wrapper-text{
 grid-column: 2/12;
    grid-row: 2;
    background-color: var(--colorN);
    border-radius: 20px;
    padding: 20px;
  }
  
  .E-section h1 {
    word-wrap: break-word;
    grid-column: 2/12;
    text-align: left;
    grid-row: 2;
    font-family: epilogue;
    font-weight: 500;
    font-size: 1.7em;
    color: white;
    margin-top: 50px;
    padding: 10px;
    line-height: 37px;
  }
  .E-section h2 {
    word-wrap: break-word;
    grid-column: 2/12;
    grid-row: 3;
    margin-top: 10px;
    font-family: epilogue;
    font-weight: 300;
    font-size: 1.2em;
    color: var(--colorC);
    text-align: left;
    padding: 10px;
    line-height: 30px;
  }
  .wrapper-spaceShip {
    padding: 50px;
    display: flex;
    justify-content: center;
    align-items: center;
    grid-column: 2/12;
    grid-row: 1;
    z-index: 0;
    background-image: url(../Assets//png-gralypho/form3.svg);
    background-repeat: no-repeat;
    background-size: 130%;
    background-position: center;
    transform: rotate(0deg);
  }
  .space-ship {
    height: 150px;
    width: 150px;
    transform: scale(0.7) rotate(50deg);
    z-index: 1;
    margin-left: 0px;
  }
</style>
