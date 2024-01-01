<script>
  import SpaceShip from "../Assets/png-gralypho/Saly-43.png";
  import Banner from "../Components/Banner.svelte";

   import square from "../Assets/png-gralypho/square.svg";

  import { onMount } from "svelte";

  onMount(() => {
    gsap.to(".gsap2", {
      scale: 1.1,
      ease: "expoScale",
      scrollTrigger: {
        trigger: ".gsap2",
        start: "top 800px",
        end: "-200px",
        scrub: 1,
      },
    });
  });
</script>

<section class="E-section" id="sectionE">
  <div class="wrapper-text">
    <img src={SpaceShip} alt="" class="space-ship gsap2" />
    <img src={square} alt="" class="square gsap2" />
    <h1>Gralypho créer un service unique de produits numériques.</h1>
    <h2>Selon vos besoins, nous utiliserons Wix, ou wordpress, ou sqarspace, Shopify, woo Commerce (...).</h2>
    <Banner />
  </div>
</section>

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
  .wrapper-text {
    grid-column: 2/12;
    grid-row: 2;
    display: flex;
    flex-direction: column;
    border-radius: 20px;
    padding: 20px;
    border: solid grey 1px;
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
    .space-ship {
    height: 170px;
    transform: scale(0.7) rotate(50deg);
    z-index: 2;
    align-self: center;
    margin-top: 50px;
  }
  .square {
    height: 150px;
    transform: scale(0.7) rotate(0deg);
    z-index: 1;
    align-self: center;
    margin-top: -150px;
  }

  .gsap2 {
    background-color: transparent;
  }


    @media screen and (max-width: 768px) {
    .E-section {
      font-size: 13px;
    }
  }
</style>
