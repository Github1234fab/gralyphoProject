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
        start: "top 440px",
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
    <h1>Exemples de réalisations d'outils digitaux</h1>
    <h2>Voici des sites témoins, comme des appartement témoins ! Chaque projet utilise une technique particulière ou met l'accent sur un design, une fonctionnalité, etc Découvrez !</h2>
<i class="fa-solid fa-arrows-left-right  arrow"></i>
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
    margin-top: 170px;
            margin-left: 30px;
    margin-right: 30px;
    border-radius: 6px;
  }
  .wrapper-text {
    grid-column: 2/12;
    grid-row: 2;
    border-radius: 20px;
    padding: 20px;
      /* border: solid 1px rgb(55, 55, 55); */
   /* background-image: url(../Assets/png-gralypho/ggglitch.svg); */
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
      font-weight: 700;
    font-size: 2.3em;
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
    transform: scale(0.4);
    opacity: 0.2;
    margin-left: 17px;
  }
  .triangle {
    height: 150px;
    z-index: 1;
    transform: scale(0.4) rotate(180deg);
    opacity: 0.2;
    align-self: center;
    margin-top: -130px;
  }

  .arrow{
    height: 40px;
    width: 40px;
    display: flex;
    justify-content: center;
    align-items: center;
    padding: 25px;
    margin-top: 20px;
   color: grey;
font-size: 2em;
opacity: 0.7;
border-radius: 50%;
border: solid grey 1px;
  }

  @media screen and (max-width: 768px) {
    .G-section {
      font-size: 13px;
    }
        .wrapper-text{
      background-size: 100%;
    }
  }
</style>
