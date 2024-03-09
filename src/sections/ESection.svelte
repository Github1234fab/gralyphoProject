<script>
  import SpaceShip from "../Assets/png-gralypho/rocketShip.png";
  import Banner from "../Components/Banner.svelte";

  import square from "../Assets/png-gralypho/square.svg";

  import { onMount } from "svelte";

  // import { tweened } from 'svelte/motion';
  // import { cubicOut } from 'svelte/easing';

  // let text = 'Découvrez toutes nos solutions 100% digitalisées';
  // let textArray = text.split('');
  // let displayText = '';
  // let delay = 100; // Délai entre chaque lettre en millisecondes

  // const count = tweened(0, {
  //   duration: textArray.length * delay,
  //   easing: cubicOut
  // });

  // count.subscribe(value => {
  //   displayText = textArray.slice(0, Math.floor(value / delay)).join('');
  // });

  onMount(() => {
    gsap.to(".space-ship", {
      scale: 1,
      duration: 5,
      y: -300,
      ease: "expoScale",
      scrollTrigger: {
        trigger: ".space-ship",
        start: "top 400px",
        end: "-200px",
        scrub: 3,
      },
    });
  });
  //   gsap.to(".E-section", {
  //     opacity: 1,
  //     ease: "E-section",
  //     scrollTrigger: {
  //       trigger: ".gsap2",
  //       start: "top 800px",
  //       end: "-200px",
  //       scrub: 3,
  //     },
  //   });
  // });
</script>

<section class="E-section" id="sectionE">
  <!-- <img src={SpaceShip} alt="illustration cartoon d'une fusée" class="space-ship" /> -->
  <div class="wrapper-text">
    <!-- <img src={square} alt="illustration cartoon d'un carré formant un cadre autour de la fusée" class="square gsap2" /> -->
    <h1>
      Nous créeons vos outils digitaux, vos designs, votre stratégie sur les réseaux et votre référencement.<br />
    </h1>

    <h2>Découvrez ici toutes <span>les solutions </span>que nous pouvons vous apporter.</h2>
    <div class="wrapper-buttons">
      <a class="contact-E" href="/#footer">Nous contacter</a>
      <a class="contact2-E" href="/#footer">Devis gratuit</a>
    </div>
    <div class="wrapper-banner">
      <Banner />
    </div>
  </div>
</section>

<style>
  .E-section {
    /* scroll-margin-top: 100px; */
    display: grid;
    grid-template-columns: repeat(12, 1fr);
    grid-template-rows: auto;
    margin-top: 100px;
    margin-bottom: 50px;
    height: auto;
    font-size: 16px;
    background-size: 150% 100%;
    shape-outside: circle(90%);
    background-color: var(--primary);
  }
  .wrapper-text {
    grid-column: 2/12;
    grid-row: 1;
    display: flex;
    flex-direction: column;
    padding: 20px;
    margin-top: 0px;
  }

  .E-section h1 {
    font-family: epilogue;
    font-size: var(--xl);
    font-weight: 800;
    text-align: left;
    color: rgb(243, 240, 240);
    margin-top: 70px;
    letter-spacing: -2px;
    line-height: 55px;
  }
  .E-section h1 span {
    font-weight: 900;
    color: transparent;
    -webkit-background-image: linear-gradient(to left, var(--blue2), var(--orange));
    background-image: linear-gradient(to left, var(--blue2), var(--orange));
    -webkit-background-clip: text;
    background-clip: text;
    letter-spacing: 0px;
  }
  .E-section h2 {
    font-family: poppins;
    font-weight: 300;
    font-size: var(--m);
    color: rgb(174, 173, 173);
    text-align: left;
    line-height: 30px;
    margin-top: 20px;
    margin-left: 0px;
  }
  .E-section h2 span {
    font-weight: 800;
    color: rgb(193, 193, 193);
  }
  /* .space-ship {
    height: 150px;
    transform: rotate(22deg) translateX(600px);
    z-index: 2;
    align-self: center;
    grid-column: 12;
    grid-row: 1;
  } */
  /* .wrapper-banner {
    grid-column: 1/13;
    grid-row: 2;
    margin: 0 auto;
  } */
  /* .square {
    height: 150px;
    transform: scale(0.7) rotate(0deg);
    z-index: 1;
    align-self: center;
    margin-top: -150px;
  } */
  .wrapper-buttons {
    margin-top: 50px;
    display: flex;
  }
  .contact-E {
    text-decoration: none;
    color: white;
    background-color: var(--CTA);
    font-family: kanit;
    font-weight: 400;
    margin-top: 30px;
    margin-left: 0px;
    width: 160px;
    border-radius: 6px;
    text-align: center;
    padding: 20px;
    box-shadow: 0px 0px 10px 2px rgba(76, 76, 76, 0.35);
  }
  .contact2-E {
    text-decoration: none;
    color: white;
    background-image: linear-gradient(to left, var(--orange), var(--CTA));
    font-family: kanit;
    font-weight: 400;
    margin-top: 30px;
    margin-left: 10px;
    width: 160px;
    border-radius: 6px;
    text-align: center;
    padding: 20px;
    box-shadow: 0px 0px 10px 2px rgba(76, 76, 76, 0.35);
  }
  .contact-E:hover,
  .contact2-E:hover {
    animation: bounce 0.4s ease-in-out;
  }
  @keyframes bounce {
    0% {
      transform: scale(1) translateY(-2px);
    }
    25% {
      transform: scale(1) translateY(3px);
    }
    50% {
      transform: scale(1) translateY(-1px);
    }
    75% {
      transform: scale(1) translateY(2px);
    }
    100% {
      transform: scale(1) translateY(0);
    }
  }

  .wrapper-banner {
    grid-column: 1/12;
    grid-row: 3;
    display: flex;
    align-items: center;
    justify-content: center;
    margin-top: 100px;
    flex-wrap: wrap;
    gap: 20px;
    margin-bottom: 100px;
    /* margin-left: auto;
    margin-right: auto; */
  }

  @media only screen and (min-width: 300px) and (max-width: 576px) {
    /* .E-section {
      font-size: 12px;
    } */
    .E-section h1 {
      line-height: 50px;
    }
  }
</style>
