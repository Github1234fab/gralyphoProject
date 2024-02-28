<script>
  import SpaceShip from "../Assets/png-gralypho/rocketShip.png";
  import Banner from "../Components/Banner.svelte";

  import square from "../Assets/png-gralypho/square.svg";

  import { onMount } from "svelte";

  onMount(() => {
    gsap.to(".gsap2", {
      scale: 1.1,
      ease: "expoScale",
      scrollTrigger: {
        trigger: ".gsap2",
        start: "top 700px",
        end: "-200px",
        scrub: 3,
      },
    });
    gsap.to(".E-section", {
      opacity: 1,
      ease: "E-section",
      scrollTrigger: {
        trigger: ".gsap2",
        start: "top 800px",
        end: "-200px",
        scrub: 3,
      },
    });
  });
</script>

<section class="E-section" id="sectionE">
  <div class="wrapper-text">
    <img src={SpaceShip} alt="illustration cartoon d'une fusée" class="space-ship gsap2" />
    <img src={square} alt="illustration cartoon d'un carré formant un cadre autour de la fusée" class="square gsap2" />
    <h1>Déclenchez enfin la révolution dans votre <span>Stratégie Numérique !</span></h1>
    <h2>Découvrez nos Solutions <span>100% </span>Digitales</h2>
    <!-- <h2>
      Vous avez besoin d'un site vitrine, d'une application android? Ou alors, votre site internet date un peu et sans
      débourser une fortune, le relooker serait plutôt sympa ?! <br />Trouvez la bonne solution par gagner du temps et de l'argent, grâce à nos solutions digitales, livrées clefs en main !
    </h2> -->
    <Banner />
  </div>
</section>

<style>
  .E-section {
    scroll-margin-top: 150px;
    display: grid;
    grid-template-columns: repeat(12, 1fr);
    grid-template-rows: auto;
    margin-bottom: 50px;
    height: auto;
    font-size: 16px;
    background-size: 150% 100%;
    shape-outside: circle(90%);
    opacity: 0.2;
  }
  .wrapper-text {
    grid-column: 2/12;
    grid-row: 2;
    display: flex;
    flex-direction: column;
    padding: 20px;
    margin-top: 100px;
  }

  .E-section h1 {
    grid-column: 2/12;
    text-align: left;
    grid-row: 2;
    font-family: epilogue;
    font-size: var(--xl);
    font-weight: 900;
    color: white;
    margin-top: 50px;
    padding: 10px;
    line-height: 53px;
  }
  .E-section h1 span {
    font-weight: 900;
    color: transparent;
    -webkit-background-image: linear-gradient(to left, var(--blue2), var(--blue));
    background-image: linear-gradient(to left, var(--blue2), var(--blue));
    -webkit-background-clip: text;
    background-clip: text;
  }
  .E-section h2 {
    word-wrap: break-word;
    grid-column: 2/12;
    grid-row: 3;
    margin-top: 10px;
    font-family: epilogue;
    font-weight: 300;
    font-size: var(--m);
    color: var(--colorC);
    text-align: left;
    padding: 10px;
    line-height: 30px;
  }
  .E-section h2 span {
    font-weight: 700;
    color: transparent;
    -webkit-background-image: linear-gradient(to left, var(--blue2), var(--blue));
    background-image: linear-gradient(to top, orange 50%, var(--blue));
    -webkit-background-clip: text;
    background-clip: text;
  }
  .space-ship {
    height: 170px;
    transform: scale(0.7) rotate(50deg);
    z-index: 2;
    align-self: center;
    margin-top: 0px;
  }
  .square {
    height: 150px;
    transform: scale(0.7) rotate(0deg);
    z-index: 1;
    align-self: center;
    margin-top: -150px;
  }

  .gsap2 {
    background-color: transparent;
  }

  @media screen and (max-width: 768px) {
    .wrapper-text {
      background-size: 100%;
    }
  }
</style>
