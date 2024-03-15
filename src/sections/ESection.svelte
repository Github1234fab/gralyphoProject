<script>
  import CardServices from "../Components/CardServices.svelte";
  const servicesTab = [
    {
      title: "Site internet",
      lien: "/Sites",
        i:   "fa-solid fa-globe",
    },
    {
      title: "Application Web",
      lien: "/Applications",
      i: "fa-solid fa-mobile-screen",
    },
    {
      title: "Design",
      lien: "/Refonte",
      i: "fa-solid fa-wand-magic-sparkles",
    },
    {
      title: "Référencement",
      lien: "/Referencement",
      i: "fa-solid fa-magnifying-glass",
    },
    {
      title: "Réseaux Sociaux",
      lien: "/Marketing",
      i: "fa-solid fa-hashtag",
    },
    {
      title: "Stratégie",
      lien: "/Composants",
      i: "fa-solid fa-chart-simple",
    },
  ];
</script>

<section class="E-section">
  <div class="wrapper-text">
    <h1>Nos Services</h1>
    <h2>Nous créeons vos outils digitaux, vos designs, votre stratégie sur les réseaux et votre référencement.</h2>
  </div>

  <div class="wrapper-cards-services">
    {#each servicesTab as service}
      <CardServices title={service.title} lien={service.lien} i={service.i} />
    {/each}
  </div>
</section>

<style>
  .E-section {
    display: grid;
    grid-template-columns: repeat(12, 1fr);
    grid-template-rows: auto;
    margin-bottom: 0px;
    height: auto;
    font-size: 16px;
    /* background-color: var(--primary); */
    background-color: var(--greyBg);  
    overflow: hidden;
  }
  .wrapper-text {
    grid-column: 2/ 12;
    grid-row: 1;
    display: flex;
    flex-direction: column;
    border-radius: 20px;
  }

  .E-section h1 {
    font-family: epilogue;
    font-size: var(--xl);
    font-weight: 800;
    text-align: left;
    color:  var(--primary);
    margin-top: 70px;
    letter-spacing: -0.03em;
    line-height: 1.2em;
  }
  .E-section h2 {
    font-family: poppins;
    font-weight: 300;
    font-size: var(--m);
    color: grey;
    text-align: left;
    line-height: 30px;
  }

  .wrapper-cards-services {
    grid-column: 2/12;
    grid-row: 2;
    display: flex;
    flex-wrap: wrap;
    align-items: center;
    justify-content: center;
    gap: 15px;
    margin-bottom: 100px;
    margin-top: 80px;
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
</style>
