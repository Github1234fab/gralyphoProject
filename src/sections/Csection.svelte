<script>
  import Robot from "../Assets/png-gralypho/Saly-39.png";
  import { onMount } from "svelte";

  onMount(() => {
    gsap.to(".robot", {
      scale: 1.1,
      ease: "expoScale",
      scrollTrigger: {
        trigger: ".robot",
        start: "top 700px",
        end: "-200px",
        scrub: 1,
      },
    });
  });
</script>

<section class="C-section">
  <div class="wrapper-image">
    <img src={Robot} alt="icon de robot en 3D" class="robot" />
  </div>
  <div class="wrapper-text">
    <h1>
      Grâce à notre expertise en création de sites Web et Apps , vous bénéficiez des meilleures technologies !
    </h1>

    <p>
      Selon vos besoins spécifiques, nous choisirons méticuleusement la technologie la plus adaptée pour la réalisation
      de votre application. <br />
      Wordpress? Wix? Shopify? From Scratch? Woo Commerce? Squarespace ? Webflow? (...) Quelle est la technologie la plus
      appropriée à la réalisation de votre site internet ou de votre application? C'est une question fondamentale parce qu'elle
      va déterminer la durée de conception, le coût et l'efficacité de votre outil en terme de rapidité, de fonctionnalité
      et de maintenance
    </p>
  </div>
</section>

<style>
  .C-section {
    display: grid;
    grid-template-columns: repeat(12, 1fr);
    grid-template-rows: 1;
    height: auto;
    font-size: 16px;
    background-color: var(--colorO);
    margin-top: 0px;
  }
  .wrapper-text {
    grid-column: 2/12;
    grid-row: 2;
    background-color: var(--colorN);
    border-radius: 20px;
    padding: 20px;
  }
  .C-section h1 {
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

  .C-section p {
    grid-column: 2/12;
    grid-row: 3;
    color: var(--colorC);
    margin-top: 20px;
    text-align: left;
    line-height: 30px;
    font-weight: 300;
    font-size: 1.1em;
    font-family: epilogue;
    padding: 10px;
  }
  .wrapper-image {
    padding: 30px;
    display: flex;
    justify-content: center;
    align-items: center;
    grid-column: 2/12;
    grid-row: 1;
    z-index: 0;
    background-image: url(../Assets//png-gralypho/form5.svg);
    background-repeat: no-repeat;
    background-size: 130%;
    background-position: center;
  }
  .robot {
    transform: rotate(0deg);
    transform: scale(0.6);
    height: 180px;
    width: 180px;
    margin-top: 50px;
    z-index: 2;
  }
</style>
