<script>
  import World from "../Assets/png-gralypho/Saly-12.png";
  import Analist from "../Assets/png-gralypho/Saly-44.png";
  import { onMount } from "svelte";
   import six from "../Assets/png-gralypho/six.svg";

  onMount(() => {
    gsap.to(".smartphone", {
      rotate: 740,
      scale: 1,
      scrollTrigger: {
        trigger: ".smartphone",
        start: "top 700px",
        end: "-300px",
        scrub: 2,
      },
    });
  });
</script>

<section class="F-section">
  <div class="wrapper-text">
    <img src={World} alt="" class="smartphone gsap3" />
    <img src={six} alt="" class="six gsap3" />
    <h1>Rérencement: SEO ou SEA?</h1>
    <h2>Selon vos besoins, nous utiliserons Wix, ou wordpress, ou sqarspace, Shopify, woo Commerce (...) ou n</h2>
  </div>
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
    border: solid 1px grey;
    border-radius: 20px;
    padding: 20px;
    display: flex;
    flex-direction: column;
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
  .smartphone {
    height: 200px;
    margin-top: 0px;
    transform: rotate(20deg);
    z-index: 2;
    align-self: center;
    margin-top: 50px;
  }
  .six {
    height: 200px;
    margin-top: -190px;
    transform: rotate(20deg);
    z-index: 1;
    align-self: center;
  }

    @media screen and (max-width: 768px) {
    .F-section {
      font-size: 13px;
    }
  }
</style>
