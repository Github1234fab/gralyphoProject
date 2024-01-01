<script>
  import Dev from "../Assets/png-gralypho/Saly-11.png";
  import Carousel from "../Components/CarousselCards.svelte";

  import { onMount } from "svelte";

  onMount(() => {
    gsap.to(".dev", {
      scale: 1.4,
      scrollTrigger: {
        trigger: ".dev",
        start: "top 700px",
        end: "-300px",
        scrub: 1,
      },
    });
  });
</script>

<section class="G-section">
  <div class="wrapper-text">
    <h1>Nos exemples de réalisations</h1>
    <h2>Selon vos besoins, nous utiliserons Wix, ou wordpress, ou sqarspace, Shopify, woo Commerce (...) ou n</h2>
  <Carousel />
  </div>
  <div class="wrapper-dev">
    <img src={Dev} alt="icon de developpeur informatique" class="dev" />
  </div>

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
  .wrapper-text {
    grid-column: 2/12;
    grid-row: 2;
    background-color: var(--colorN);
    border-radius: 20px;
    padding: 20px;
  }
  .G-section h1 {
    word-wrap: break-word;
    text-align: left;
    font-family: epilogue;
    font-weight: 500;
    font-size: 1.7em;
    color: white;
    margin-top: 50px;
    padding: 10px;
    line-height: 37px;
  }
  .G-section h2 {
    word-wrap: break-word;
    margin-top: 10px;
    font-family: epilogue;
    font-weight: 300;
    font-size: 1.2em;
    color: var(--colorC);
    text-align: left;
    padding: 10px;
    line-height: 30px;
  }
  .wrapper-dev {
    padding: 50px;
    display: flex;
    justify-content: center;
    align-items: center;
    grid-column: 2/12;
    grid-row: 1;
    z-index: 0;
    background-image: url(../Assets//png-gralypho/form1.svg);
    background-repeat: no-repeat;
    background-size: 130%;
    background-position: center;
    transform: rotate(2deg);
  }
  .dev {
    grid-column: 7;
    height: 150px;
    width: 150px;
    grid-row: 1;
    margin-left: 17px;
    z-index: 1;
    transform: scale(0.7);
  }
</style>
