<script>
  import Climber from "../Assets/png-gralypho/Saly-15.png";
  import six from "../Assets/png-gralypho/six.svg";

  import { onMount } from "svelte";

  onMount(() => {
    gsap.to(".gsap5", {
      rotate: 370,
      scale: 1,
      scrollTrigger: {
        trigger: ".gsap5",
        start: "top 600px",
        end: "-300px",
        scrub: 2,
      },
    });
  });
</script>

<section class="H-section">
  <div class="wrapper-text">
    <img src={Climber} alt="" class="climb gsap5" />
    <img src={six} alt="" class="six gsap5" />
    <h1>Les meilleurs c’est nous</h1>
    <h2>Selon vos besoins, nous utiliserons Wix, ou wordpress, ou sqarspace, Shopify, woo Commerce (...) ou n</h2>
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
    display: flex;
    flex-direction: column;
    border-radius: 20px;
    padding: 20px;
    border: solid 1px grey;
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
  .gsap5 {
    background-color: transparent;
  }

  .climb {
    height: 160px;
    margin-top: 40px;
    z-index: 2;
    align-self: center;
  }

  .six {
    height: 160px;
    margin-top: -130px;
    z-index: 1;
    align-self: center;
  }

  @media screen and (max-width: 768px) {
    .H-section {
      font-size: 13px;
    }
  }
</style>
