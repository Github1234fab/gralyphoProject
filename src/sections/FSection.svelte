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
        scrub: 2,
      },
    });
  });
</script>

<section class="F-section">
  <h1>Rérencement: SEO ou SEA?</h1>
  <h2>Selon vos besoins, nous utiliserons Wix, ou wordpress, ou sqarspace, Shopify, woo Commerce (...) ou n</h2>
  <img src={World} alt="" class="smartphone" />
  <img src={Analist} alt="" class="world" />
  <p>
    Lorem, ipsum dolor sit amet consectetur adipisicing elit. Minima sequi corporis, fuga doloribus beatae non neque.
    Incidunt illo, totam minima soluta id est doloribus dolores laborum, magni, repellendus mollitia eos?
  </p>
  <div class="halo"></div>
</section>

<style>
  .F-section {
    display: grid;
    grid-template-columns: repeat(12, 1fr);
    grid-template-rows: auto;
    height: 100%;
    font-size: 16px;
    background-color: var(--colorO);
    margin-top: 170px;
  }
  .F-section h1 {
    grid-column: 5/12;
    grid-row: 1;
    font-family: epilogue;
    font-weight: bolder;
    font-size: 1.8em;
    color: white;
    text-transform: uppercase;
  }
  .F-section h2 {
    grid-column: 5/12;
    grid-row: 1;
    margin-top: 70px;
    font-family: epilogue;
    font-weight: 300;
    font-size: 1.2em;
    color: var(--colorC);
  }
  .F-section p {
    grid-column: 2/12;
    grid-row: 2;
    color: var(--colorC);
    margin-top: 30px;
    text-align: justify;
    font-weight: 300;
  }
  .world {
    grid-column: 2/4;
    grid-row: 1;
    height: 120px;
    width: 120px;
    margin-left: 0px;
    margin-top: 20px;
    z-index: 2;
  }
  .smartphone {
    grid-column: 2/4;
    grid-row: 1;
    height: 200px;
    width: 200px;
    margin-top: -40px;
    transform: rotate(20deg);
    z-index: 1;
  }
  .halo {
    grid-column: 2/4;
    grid-row: 1;
    background-color: rgb(79, 68, 235);
    width: 130px;
    height: 130px;
    border-radius: 50%;
    filter: blur(30px);
    z-index: 0;
    margin-left: 30px;
    margin-top: 0px;
  }
  @media screen and (max-width: 768px) {
    .F-section {
      font-size: 10px;
    }
  }

    @media screen and (max-width: 400px) {
  .world {
    height: 80px;
    width: 80px;
  }
  .smartphone {
    height: 160px;
    width: 160px;
  }
  .halo {
    width: 90px;
    height: 90px;
  }
}
</style>
