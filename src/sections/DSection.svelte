<script>
  import Check from "../Assets/png-gralypho/Saly-26.png";
  import CardsSectionB from "../Components/CardsSectionB.svelte";
  import { onMount } from "svelte";
  import circle from "../Assets/png-gralypho/circle.svg";

  onMount(() => {
    gsap.to(".gsap1", {
      scale: 1,
      ease: "expoScale",
      scrollTrigger: {
        trigger: ".gsap1",
        start: "top 670px",
        end: "-200px",
        scrub: 1,
      },
    });
       gsap.to(".D-section", {
opacity: 1,
      ease: "D-section",
      scrollTrigger: {
        trigger: ".D-section",
        start: "top 500px",
        end: "-200px",
        scrub: 1,
      },
    });
  });

  let infosCards = [
    {
      key: 1,
      title: "Votre projet est unique",
      p: "Toute réalisation, si nous souhaitons qu'elle aboutisse au résultat escompté, passe par l'écoute active de votre projet. C'est en vous écoutant attentivement et en analysant vos besoins précisément que nous pourrons déterminer le cahier des charges de votre outil digital.",
      icon: "bi bi-megaphone",
      number: "1  ",
    },
    {
      key: 2,
      title: "Cahier des charges.",
      p: "À l'issue de notre premier rendez-vous, nous aurons recueillis assez d'informations pour définir les fondations de votre outil. Son Design, son Architecture, ses Fonctionnalités, sa Dynamique et sa Sécurité. Cette phase de créativité est trépidante et vous recevrez à chaque étape un compte rendu de l'avancée de votre projet.  ",
      icon: "bi bi-feather",
      number: "2",
    },
    {
      key: 3,
      title: "Réalisation",
      p: "Votre outil, Site internet ou Application est maintenant réalisé dans sa version Bêta. C'est à dire que votre outil Digital en est à l'étape de test juste avant sa mise en ligne! C'est l'occasion de le tester en grandeur nature et nous le testerons ensemble.",
      icon: "bi bi-nut-fill",
      number: "3",
    },
    {
      key: 4,
      title: "Validation",
      p: "Après validation de la version bêta, c'est la fameuse étape de la mise en ligne et de la livraison de votre outil. C'est un rendez-vous palpitant, celui de l'utilisation de votre outil sous toutes ses coutures et de l'ultime mise en route. Ça y est! Vous possédez votre outil Digital!",
      icon: "bi bi-hand-thumbs-up",
      number: "4",
    },
  ];
</script>

<section class="D-section">
  <div class="wrapper-text">
    <!-- <div class="wrapper-check"> -->
    <img src={Check} alt="" class="check gsap1" />
    <img src={circle} alt="" class="circle gsap1" />
    <!-- </div> -->
    <h1>Les 4 étapes pour obtenir un outil digital, gagnant sur le Web !</h1>
    <h2>
      Notre expertise dans le domaine digital nous permet aujourdhui de construire des sites webs et des applications
      gagnantes sur le Web, en suivant un process de création optimal. Nous gagnons ainsi du temps et vous économisez de
      l'argent !.
    </h2>
    <div class="wrapper-accordeon">
      {#each infosCards as card}
        <CardsSectionB title={card.title} p={card.p} number={card.number} />
      {/each}
    </div>
  </div>
</section>

<style>
  .D-section {
    display: grid;
    grid-template-columns: repeat(12, 1fr);
    grid-template-rows: auto;
    height: auto;
    margin-top: 150px;
    font-size: 16px;
    /* background: radial-gradient(circle at top, var(--colorN), var(--colorO));
    background-size: 100% 100%;
    shape-outside: circle(90%); */
    margin-left: 30px;
    margin-right: 30px;
    border-radius: 6px;
    opacity: 0.2;
  }
  .wrapper-text {
    /* border: solid 1px rgb(55, 55, 55); */
    /* background-image: url(../Assets/png-gralypho/ggglitch.svg); */
    background-repeat: no-repeat;
    background-position: top;
    background-size: 20%;
    grid-column: 2/12;
    grid-row: 2;
    display: flex;
    flex-direction: column;
    /* background-color: var(--colorN); */
    border-radius: 20px;
    padding: 20px;
  }
  .D-section h1 {
    word-wrap: break-word;
    grid-column: 2/12;
    text-align: left;
    grid-row: 2;
    font-family: epilogue;
     font-size: 2.4em;
    font-weight: 800;
    color: white;
    margin-top: 50px;
    padding: 10px;
    line-height: 45px;
  }

  .D-section h2 {
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
  .check {
    margin-top: 50px;
    height: 150px;
    width: 80px;
    z-index: 1;
    transform: scale(0.7);
    align-self: center;
  }
  .circle {
    height: 180px;
    z-index: 1;
    transform: scale(0.7);
    align-self: center;
    margin-top: -130px;
  }
  .gsap1 {
    background-color: transparent;
  }
  .wrapper-accordeon {
    grid-column: 2/12;
    grid-row: 4;
    height: 100%;
    width: 100%;
    margin-top: 50px;
    font-size: 1em;
    /* background-color: var(--colorD); */
    display: flex;
    flex-direction: column;
    align-items: center;
    gap: 30px;
  }

  @media screen and (max-width: 768px) {
    .D-section {
      font-size: 13px;
    }
    .wrapper-text {
      background-size: 100%;
    }
  }
</style>
