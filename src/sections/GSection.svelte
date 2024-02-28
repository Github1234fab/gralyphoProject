<script>
  import Dev from "../Assets/png-gralypho/dev.png";
  import Carousel from "../Components/CarousselCards.svelte";
  import skate from "../Assets/png-gralypho/skateboard.png";

  import { onMount } from "svelte";

  onMount(() => {
    gsap.to(".wrapper-developpeur", {
      x:700,
      scrollTrigger: {
        trigger: ".wrapper-developpeur",
        start: "top 720px",
        end: "-100px",
        scrub: 5,
      },
    });
  });
</script>

<section class="G-section">
  <div class="wrapper-text">
    <div class="wrapper-developpeur">
    <img src={Dev} alt="illustration cartoon d'un développeur informatique" class="dev" />
    <img src={skate} alt="" class="skate" /> 
    </div>
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
    background-color: rgb(239, 237, 237);
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
    margin-top: -30px;
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
    font-size: var(--m);
   color: var(--primary);
    text-align: left;
    padding: 10px;
    line-height: 30px;
  }
  .wrapper-developpeur {
    display: flex;
    flex-direction: column;
    align-items: center;
    justify-content: center;
    margin-top: 40px;
    transform: translateX(-300px);
    width: 50px;
  }
  .dev {
    height: 150px;
    margin-top: 50px;
    z-index: 2;
    align-self: center;
    margin-left: 26px;
  }
  .skate{
    height: 50px;
    z-index: 1;
    opacity: 1;
    align-self: center;
    margin-top: -20px;
  }



  @media screen and (max-width: 768px) {
    
    .wrapper-text {
      background-size: 100%;
    }
  }
</style>
