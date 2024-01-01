<script>
  import TestimonyCards from "../Components/TestimonyCards.svelte";
  import profilOne from "../Assets/Profils-gralypho/Ellipse 43.png";
  import profilTwo from "../Assets/Profils-gralypho/Ellipse 46.png";
  import profilThree from "../Assets/Profils-gralypho/Ellipse 54.png";
  import profilFour from "../Assets/Profils-gralypho/Ellipse 63.png";

  let dataCard = [
    {
      img: profilOne,
      alt: "Photo de profil client",
      title: "SOPEGO",
      job: "CTO",
      p: "Lorem ipsum dolor sit amet consectetur adipisicing elit. Quisquam, voluptatum.",
    },
    {
      img: profilTwo,
      alt: "Photo de profil client",
      title: "Titre 2",
      job: "CTO",
      p: "Lorem ipsum dolor sit amet consectetur adipisicing elit. Quisquam, voluptatum.",
    },
    {
      img: profilThree,
      alt: "Photo de profil client",
      title: "Titre 3",
      job: "CTO",
      p: "Lorem ipsum dolor sit amet consectetur adipisicing elit. Quisquam, voluptatum.",
    },
    {
      img: profilFour,
      alt: "Photo de profil client",
      title: "Titre 3",
      job: "CTO",
      p: "Lorem ipsum dolor sit amet consectetur adipisicing elit. Quisquam, voluptatum.",
    },
  ];
</script>

<section class="J-section">
  <div class="wrapper-contain">
    <h1>Témoignages de nos clients</h1>
    <h2>Collaborations, Missions, Partenariats</h2>
    <div class="wrapper-testimony">
      {#each dataCard as card}
        <TestimonyCards title={card.title} job={card.job} p={card.p} img={card.img} alt={card.alt} />
      {/each}
    </div>
  </div>
</section>

<style>
  .J-section {
    display: grid;
    grid-template-columns: repeat(12, 1fr);
    grid-template-rows: auto;
    height: auto;
    font-size: 16px;
    margin-top: 100px;
  }
  .wrapper-contain {
    grid-column: 2/12;
    grid-row: 2;
    display: flex;
    flex-direction: column;
    border-radius: 20px;
    padding: 20px;
    border: solid 1px grey;
  }
  .J-section h1 {
    grid-column: 2/12;
    grid-row: 1;
    font-family: epilogue;
    font-weight: 600;
    font-size: 1.7em;
    color: white;
  }
  .J-section h2 {
    grid-column: 2/12;
    grid-row: 1;
    margin-top: 50px;
    font-family: epilogue;
    font-weight: 300;
    font-size: 1.2em;
    color: white;
  }
  .wrapper-testimony {
    grid-column: 2/12;
    grid-row: 2;
    display: flex;
    flex-direction: column;
    flex-wrap: wrap;
    gap: 20px;
    align-items: center;
    margin-top: 50px;
  }

  @media screen and (max-width: 768px) {
    .J-section {
      font-size: 13px;
    }
  }
</style>
