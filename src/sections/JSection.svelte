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
      job: "Patricia - Directrice",
      p: "Nous avons travaillé à plusieurs reprises avec l'agence Gralypho. En premier lieu, nous avons demandé une refonte partielle de notre site. Puis nous avons par la suite demandé une application pour faciliter le travail de nos commerciaux, principalement en interne. Ce fût une réussite! Puis de fil en aiguille, nous avons demander la réalisation de notre tout nouveau site internet. Merci à l'agence Gralypho pour avoir toujours la patience de nous écouter et de structurer nos idées, en les transformant ensuite en outil digital, qui nous correspondent absolument!",
    },
    {
      img: profilTwo,
      alt: "Photo de profil client",
      title: "ElectriKcity",
      job: "Damien - Électricien indépendant",
      p: "Quand j'ai monté ELECTRICITY à Orléans, j'entendais tout le temps mes clients me demander si j'avais un site. Moi, j'avais seulement une carte de visite à l'époque !. J'ai fait appel à l'agence Gralypho et nosu avons collaboré tout en visio. Au début j'étais toujours sceptique pour l'idée d'avoir un site internet , mais l'agence Gralypho a su me démontrer tout l'avantage d'en avoir un. L'ajout de fonctionnalité comme la prise de RV en ligne et les paiements en ligne m'ont grandement faciliter la tâche et fait gagner beaucoup de temps. Merci encore !!",
    },
    {
      img: profilThree,
      title: "Orange",
      job: "Iris - Chargée de communication",
      p: "L'agence Gralypho a su nous livrer nos composants web dans les délais! Le Design est au rendez-vous et la qualité du code aussi! Merci à toute l'équipe et bonne route!",
    },
    {
      img: profilFour,
      title: "Green NRJ",
      job: "Arjun Ramanujan",
      p: "Hello Gralypho! It was great working with you. Our specifications were complicated, but you met the challenge! The design is brilliant and the code is clean and super efficient. Our application is running at maximum! Thanks again for the collaboration. Best Freelancer based in Europe! Well done! Looking forward to a new collaboration.",
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
    margin-top: 10px;
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
