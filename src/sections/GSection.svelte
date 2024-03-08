<script>
  import Dev from "../Assets/png-gralypho/dev.png";
  import Carousel from "../Components/CarousselCards.svelte";
  import skate from "../Assets/png-gralypho/skateboard.png";
  import { onMount } from "svelte";
  import { bounceIn } from "svelte/easing";
  import Ville from "../Assets/png-gralypho/ville.png";

  onMount(() => {
    function handleResize() {
      if (window.innerWidth < 576) {
        gsap.to(".wrapper-developpeur", {
          x: 200,
          // ease: power4,
          scrollTrigger: {
            trigger: ".wrapper-developpeur",
            start: "top 920px",
            end: "-100px",
            scrub: 5,
          },
        });
      }
      else if (window.innerWidth < 768) {
        gsap.to(".wrapper-developpeur", {
          x: 400,
          // ease: power4,
          scrollTrigger: {
            trigger: ".wrapper-developpeur",
            start: "top 920px",
            end: "-100px",
            scrub: 5,
          },
        });
      } else {
        gsap.to(".wrapper-developpeur", {
          x: 700,
          // ease: power4,
          scrollTrigger: {
            trigger: ".wrapper-developpeur",
            start: "top 920px",
            end: "-100px",
            scrub: 5,
          },
        });
      }
    }

    // Appeler la fonction de gestion de redimensionnement au chargement initial
    handleResize();

    // Ajouter un écouteur d'événement pour le redimensionnement de la fenêtre
    window.addEventListener("resize", handleResize);

    // Nettoyer l'écouteur d'événement lors de la destruction du composant
    return () => {
      window.removeEventListener("resize", handleResize);
    };
  });
</script>

<section class="G-section">
  <div class="wrapper-developpeur">
    <img src={Dev} alt="illustration cartoon d'un développeur informatique" class="dev" />
    <img src={skate} alt="" class="skate" />
  </div>
  <img src={Ville} alt="png d'une ville en frise" class="ville" />
  <div class="pavement"></div>
  <div class="wrapper-text">
    <h1>Découvrez nos <span>réalisations </span></h1>
    <h2>
      Découvrez ici des projets témoins utilisant chacun une technique particulière. Découvrez vite le potentiel des
      animations, des applications, des requêtes API, des jeux, des composants. (...) !
    </h2>
  </div>
  <Carousel />
</section>

<style>
  .G-section {
    display: grid;
    grid-template-columns: repeat(12, 1fr);
    grid-template-rows: auto;
    height: auto;
    font-size: 16px;
    background-color: rgb(255, 255, 255);
  }
  .wrapper-text {
    grid-column: 2/12;
    grid-row: 2;
    display: flex;
    flex-direction: column;
    align-items: baseline;
    justify-content: baseline;
    margin-top: 50px;
  }
  .G-section h1 {
    text-align: left;
    font-family: epilogue;
    font-weight: 900;
    font-size: var(--xl);
    color: var(--primary);
    letter-spacing: -1px;
    line-height: 50px;
  }
  .G-section h1 span {
    font-weight: 900;
    color: transparent;
    -webkit-background-image: linear-gradient(to left, var(--ca), var(--blue));
    background-image: linear-gradient(to left, var(--ca), var(--blue));
    -webkit-background-clip: text;
    background-clip: text;
  }

  .G-section h2 {
    margin-top: 10px;
    font-family: poppins;
    font-weight: 300;
    font-size: var(--m);
    color: grey;
    text-align: left;
    line-height: 25px;
    letter-spacing: -1px;
  }
  .wrapper-developpeur {
    display: flex;
    flex-direction: column;
    align-items: center;
    justify-content: center;
    margin-top: -10px;
    transform: translateX(-300px);
    width: 50px;
  }
  .ville {
    grid-column: 1/12;
    grid-row: 1;
    width: auto;
    height: 500px;
    margin: 0 auto;
    margin-top: -150px;
  }
  .dev {
    height: 150px;
    margin-top: 48px;
    z-index: 2;
    align-self: center;
    margin-left: 26px;
  }
  .skate {
    height: 50px;
    z-index: 1;
    opacity: 1;
    align-self: center;
    margin-top: -24px;
  }
  .pavement {
    grid-column: 1/12;
    grid-row: 2;
    width: 100vw;
    background-image: linear-gradient(to right, var(--blue2), var(--orange));
    height: 5px;
    margin-top: -16px;
    box-shadow: 0px 10px 10px 2px rgba(76, 76, 76, 0.35);
  }

  @media screen and (max-width: 768px) {
    .wrapper-text {
      background-size: 100%;
    }
  }
</style>
