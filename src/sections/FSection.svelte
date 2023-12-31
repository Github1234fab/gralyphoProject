<script>
  import World from "../Assets/png-gralypho/Saly-12.png";
  import Analist from "../Assets/png-gralypho/Saly-44.png";
  import { onMount } from "svelte";

  onMount(() => {
    gsap.to(".smartphone", {
      rotate: 390,
      scale: 1,
      scrollTrigger: {
        trigger: ".smartphone",
        start: "top 600px",
        end: "-300px",
        scrub: 1,
      },
    });
  });
</script>

<section class="F-section">
  <div class="wrapper-text">
    <h1>Rérencement: SEO ou SEA?</h1>
    <h2>Selon vos besoins, nous utiliserons Wix, ou wordpress, ou sqarspace, Shopify, woo Commerce (...) ou n</h2>
  </div>
  <div class="wrapper-smartphone">
    <img src={World} alt="" class="smartphone" />
  </div>
  <div class="halo"></div>
</section>

<style>
  .F-section {
    display: grid;
    grid-template-columns: repeat(12, 1fr);
    grid-template-rows: auto;
    height: auto;
    font-size: 16px;
    background-color: var(--colorO);
    margin-top: 170px;
    margin-bottom: 100px;
  }
  .wrapper-text {
    grid-column: 2/12;
    grid-row: 2;
    background-color: var(--colorN);
    border-radius: 20px;
    padding: 20px;
  }
  .F-section h1 {
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
  .F-section h2 {
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
  .wrapper-smartphone {
    padding: 50px;
    display: flex;
    justify-content: center;
    align-items: center;
    grid-column: 2/12;
    grid-row: 1;
    z-index: 0;
    background-image: url(../Assets//png-gralypho/form2.svg);
    background-repeat: no-repeat;
    background-size: 130%;
    background-position: center;
    transform: rotate(1deg);
  }
  .smartphone {
    height: 200px;
    width: 200px;
    margin-top: 0px;
    transform: rotate(20deg);
    z-index: 1;
  }
</style>
