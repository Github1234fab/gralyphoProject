<script>
  import Check from "../Assets/png-gralypho/Saly-26.png";
  import CardsSectionB from "../Components/CardsSectionB.svelte";
  import { onMount } from "svelte";

  onMount(() => {
    gsap.to(".check", {
      scale: 1.2,
      ease: "expoScale",
      scrollTrigger: {
        trigger: ".check",
        start: "top 600px",
        end: "-200px",
        scrub: 2,
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
  <h1>Nos process de créations sont stables et testés.</h1>
  <h2>lls nous permettent de créer des produits Digitaux 100% efficace et correspondants formellement à vos besoins</h2>
  <img src={Check} alt="" class="check" />

  <div class="wrapper-accordeon">
    {#each infosCards as card}
      <CardsSectionB title={card.title} p={card.p} number={card.number} />
    {/each}
  </div>
  <div class="halo"></div>
</section>

<style>
  .D-section {
    display: grid;
    grid-template-columns: repeat(12, 1fr);
    grid-template-rows: auto;
    height: 700px;
    margin-top: 150px;
    font-size: 16px;
    background-color: var(--colorO);
  }
  .D-section h1 {
    grid-column: 2/7;
    grid-row: 1;
    font-family: epilogue;
    font-weight: bolder;
    font-size: 1.8em;
    font-weight: 600;
    color: white;
    text-transform: uppercase;
  }
  .D-section h2 {
    grid-column: 2/7;
    grid-row: 1;
    margin-top: 110px;
    font-family: epilogue;
    font-weight: 300;
    font-size: 1.2em;
    color: var(--colorC);
  }
  .check {
    grid-column: 9;
    grid-row: 1;
    height: 100px;
    width: 80px;
    z-index: 1;
    transform: scale(0.7);
  }
  .wrapper-accordeon {
    grid-column: 2/12;
    grid-row: 2;
    height: 100%;
    width: 100%;
    margin-top: 50px;
    font-size: 1em;
    /* background-color: var(--colorD); */
    display: flex;
    flex-direction: column;
    align-items: center;
  }
  .halo {
    grid-column: 9;
    grid-row: 1;
    background-color: rgb(79, 68, 235);
    width: 100px;
    height: 100px;
    border-radius: 50%;
    filter: blur(30px);
    z-index: 0;
    margin-left: 0px;
    margin-top: 0px;
  }
  @media screen and (max-width: 768px) {
    .D-section {
      font-size: 10px;
    }
  }
  @media screen and (max-width: 375px) {
    .D-section h2 {
      grid-column: 2/12;
      margin-top: 200px;
    }
  }
</style>
