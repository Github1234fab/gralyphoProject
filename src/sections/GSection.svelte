<script>
  import Dev from "../Assets/png-gralypho/Saly-11.png";
  import Carousel from "../Components/CarousselCards.svelte";
  import triangle from "../Assets/png-gralypho/nnneon (6).svg";

  import { onMount } from "svelte";

  onMount(() => {
    gsap.to(".gsap4", {
      scale: 1.3,
      opacity: 1,
      scrollTrigger: {
        trigger: ".gsap4",
        start: "top 740px",
        end: "-300px",
        scrub: 3,
      },
    });
  });
</script>

<section class="G-section">
  <div class="wrapper-text">
    <img src={Dev} alt="icon de developpeur informatique" class="dev gsap4" />
    <!-- <img src={triangle} alt="icon de developpeur informatique" class="triangle gsap4" /> -->
    <h1>Découvrez nos <span>réalisations </span></h1>
    <h2>
      Voici des sites témoins...comme des appartement témoins. Chaque projet utilise une technique particulière ou met
      l'accent sur un design, une fonctionnalité, etc. Découvrez vite le potentiel des animations, des applications de météo, des jeux, des composants... !
    </h2>
    <Carousel />
  </div>
</section>

<style>
  .G-section {
    display: grid;
    grid-template-columns: repeat(12, 1fr);
    grid-template-rows: auto;
    height: auto;
    font-size: 16px;
    background-color: var(--colorC);
  }
  .wrapper-text {
    grid-column: 2/12;
    grid-row: 2;
    border-radius: 20px;
    padding: 20px;
    background-repeat: no-repeat;
    background-position: top;
    background-size: 30%;
    display: flex;
    flex-direction: column;
  }
  .G-section h1 {
    word-wrap: break-word;
    text-align: left;
    font-family: epilogue;
    font-weight: 900;
    font-size: var(--xl);
    color: var(--primary);
    margin-top: 50px;
    padding: 10px;
    line-height: 37px;
  }
.G-section h1 span{
  font-weight: 900;
  color: transparent;
  -webkit-background-image: linear-gradient(to left, var(--ca), var(--blue));
  background-image: linear-gradient(to left, var(--ca), var(--blue));
  -webkit-background-clip: text;
  background-clip: text;
}

  .G-section h2 {
    word-wrap: break-word;
    margin-top: 10px;
    font-family: epilogue;
    font-weight: 300;
    font-size: var(--l);
   color: var(--primary);
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
    transform: scale(0.4);
    opacity: 0.2;
    margin-left: 26px;
  }
  /* .triangle {
    height: 150px;
    z-index: 1;
    transform: scale(0.4) rotate(0deg);
    opacity: 0.2;
    align-self: center;
    margin-top: -140px;
  } */



  @media screen and (max-width: 768px) {
    
    .wrapper-text {
      background-size: 100%;
    }
  }
</style>
