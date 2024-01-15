<script>
  import { onMount } from "svelte";
  import TestimonyCards from "../Components/TestimonyCards.svelte";
  import profilOne from "../Assets/Profils-gralypho/Frame (2).png";
  import profilTwo from "../Assets/Profils-gralypho/Frame (5).png";
  import profilThree from "../Assets/Profils-gralypho/Frame (12).png";
  import profilFour from "../Assets/Profils-gralypho/Ellipse 125.png";
  import profilFive from "../Assets/Profils-gralypho/Ellipse 131.png";
  import profilSix from "../Assets/Profils-gralypho/Ellipse 220.png";

  onMount(() => {
    gsap.to(".J-section", {
      opacity: 1,
      ease: "expoScale",
      scrollTrigger: {
        trigger: ".J-section",
        start: "top 400px",
        end: "-200px",
        scrub: 4,
      },
    });
  });

  let dataCard = [
    {
      img: profilTwo,
      title: "Mademoiselle G.",
      job: "Marjolaine - Directrice de la communicaiton",
      p: "Délai respecté, composants fonctionnels avec une très bonne intégration. Nous recommandons Gralypho! ",
    },
    {
      img: profilFive,
      alt: "Photo de profil client",
      title: "ElectriKcity",
      job: "Damien - Électricien indépendant",
      p: "L'ajout de fonctionnalité comme la prise de RV et les paiements en ligne m'ont grandement faciliter la tâche et fait gagner beaucoup de temps et de l'argent! Merci encore pour l'accompagnement.",
    },
    {
      img: profilThree,
      title: "Green NRJ",
      job: "Asha Ramanujan - Project Manager",
      p: "Hello Gralypho! It was great working with you. Our specifications were complicated, but you met the challenge! The design is brilliant and the code is clean and super efficient. Our application is running at maximum! ",
    },
    {
      img: profilFour,
      title: "Sepocat",
      job: "Christophe Muun - Styliste",
      p: "Enfin un professionnel ! Merci pour notre application, elle est parfaite! ",
    },
    {
      img: profilSix,
      title: "Le Marminot",
      job: "Hugo Hervé - Restaurateur",
      p: "Merci pour toutes les idées qui permettent à nos clients de découvrir notre restauration, comme jamais!",
    },
    {
      img: profilOne,
      title: "Inès Marjot",
      job: "Photographe",
      p: "Plus de clients, moins de temps perdu, plus d'argent.... it's perfect Gralypho!!",
    },
  ];
</script>

<section class="J-section">
  <h1>Témoignages de nos clients</h1>
  <h2>Collaborations, Missions, Partenariats.</h2>
  <div class="gallery">
    <div class="wrapper-contain">
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
    margin-top: 0px;
    opacity: 0.2;
    background-color: var(--colorC);
     background-image: url(../Assets/png-gralypho/waves4.svg);
    background-repeat: no-repeat;
    background-size: cover;
  }
  .gallery {
    overflow-x: auto;
    grid-column: 1/13;
    grid-row: 2;
    margin-left: 200px;
  }
  .wrapper-contain {
    display: flex;
    flex-direction: row;
    flex-wrap: nowrap;
    border-radius: 20px;
    justify-content: start;
    align-items: center;
    margin-bottom: 30px;
    gap: 20px;
  }
  .J-section h1 {
    grid-column: 1/12;
    grid-row: 1;
    font-family: epilogue;
    font-size: 2.7em;
    font-weight: 800;
    color: var(--primay);
    margin-left: 100px;
    margin-top: 100px;
  }
  .J-section h2 {
    grid-column: 2/12;
    grid-row: 1;
    margin-top: 10px;
    font-family: epilogue;
    font-weight: 300;
    font-size: 1.2em;
    color: white;
    margin-left: 100px;
  }
  /* .wrapper-testimony {
    display: flex;
    align-items: flex-start;
    justify-content: center;
    flex-wrap: wrap;
    gap: 40px;
    margin-top: 50px;
  } */

  @media screen and (max-width: 768px) {
    .J-section {
      font-size: 14px;
    }
    .gallery {
    overflow-x: auto;
    grid-column: 1/13;
    grid-row: 2;
    margin-left: 20px;
  }
  .J-section h1 {
    grid-column: 1/12;
    grid-row: 1;
    font-family: epilogue;
    font-size: 2.7em;
    font-weight: 800;
    color: var(--primay);
    margin-left: 50px;
    margin-top: 100px;
  }
  }
</style>
