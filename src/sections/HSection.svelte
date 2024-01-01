<script>
  import Climber from "../Assets/png-gralypho/Saly-15.png";

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
    });
  });
</script>

<section class="H-section">
  <div class="wrapper-text">
    <h1>Les meilleurs c’est nous</h1>
    <h2>Selon vos besoins, nous utiliserons Wix, ou wordpress, ou sqarspace, Shopify, woo Commerce (...) ou n</h2>
  </div>
  <div class="wrapper-climber">
  <img src={Climber} alt="" class="climb" />
  </div>
 
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
  .wrapper-text {
    grid-column: 2/12;
    grid-row: 2;
    background-color: var(--colorN);
    border-radius: 20px;
    padding: 20px;
  }
  .H-section h1 {
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
  .H-section h2 {
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
  .wrapper-climber{
	 padding: 50px;
    display: flex;
    justify-content: center;
    align-items: center;
    grid-column: 2/12;
    grid-row: 1;
    z-index: 0;
    background-image: url(../Assets//png-gralypho/form4.svg);
    background-repeat: no-repeat;
    background-size: 130%;
    background-position: center;
    transform: rotate(2deg);
  }
  .climb {
    grid-column: 2/3;
    height: 160px;
    width: 100px;
    grid-row: 1;
    margin-top: -30px;
    z-index: 1;
  }
  
</style>
