<script>
  import Dev from "../Assets/png-gralypho/Saly-11.png";
  import Carousel from "../Components/CarousselCards.svelte";
  import triangle from "../Assets/png-gralypho/nnneon (6).svg";

  import { onMount } from "svelte";

  onMount(() => {
    gsap.to(".gsap4", {
      scale: 1.2,
      opacity: 1,
      scrollTrigger: {
        trigger: ".gsap4",
        start: "top 500px",
        end: "-300px",
        scrub: 1,
      },
    });
  });
</script>

<section class="G-section">
  <div class="wrapper-text">
    <img src={Dev} alt="icon de developpeur informatique" class="dev gsap4" />
    <img src={triangle} alt="icon de developpeur informatique" class="triangle gsap4" />
    <h1>Nos exemples de réalisations</h1>
    <h2>Selon vos besoins, nous utiliserons Wix, ou wordpress, ou sqarspace, Shopify, woo Commerce (...) ou n</h2>
    <Carousel />
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
    border-radius: 20px;
    padding: 20px;
    border: solid 1px grey;
    display: flex;
    flex-direction: column;
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
  .gsap4 {
    background-color: transparent;
  }
  .dev {
    height: 150px;
    margin-top: 50px;
    z-index: 2;
    align-self: center;
    transform: scale(0.4) opacity(0.2);
    margin-left: 30px;
  }
  .triangle {
    height: 150px;
    z-index: 1;
    transform: scale(0.4) rotate(180deg) opacity(0.2);
    align-self: center;
    margin-top: -130px;
  }

    @media screen and (max-width: 768px) {
    .G-section {
      font-size: 13px;
    }
  }
</style>
