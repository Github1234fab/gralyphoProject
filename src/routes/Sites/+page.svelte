<script>
  import { fade, slide } from "svelte/transition";
  // import bg from "../../Assets/png-gralypho/41.png";
  import Header from "../../sections/Header.svelte";
  // import vitrine from "../../Assets/png-gralypho/vitrine.svg";
  import portfolio from "../../Assets/png-gralypho/address-card-regular.svg";
  import commerce from "../../Assets/png-gralypho/shopping.svg";
  import blog from "../../Assets/png-gralypho/blog-solid.svg";
  import corporate from "../../Assets/png-gralypho/user-tie-solid.svg";
  import institution from "../../Assets/png-gralypho/building-columns-solid.svg";
  import Engrenages from "../../Components/Engrenages.svelte";
  import imgHero from "../../Assets/png-gralypho/webExplosion.png";
  import CardsSites from "../../Components/CardsSites.svelte";
  import FSection from "../../sections/FSection.svelte";
  import Profits from "../../sections/SectionProfitsSite.svelte";

  let sitesTab = [
    {
      type: "Site Vitrine",
      description:
        "Le site Vitrine a pour objectif de présenter votre entreprise, vos services, vos produits, vos valeurs, votre équipe, vos actualités,  etc. Mis à part un formulaire de contact, ce type de site ne propose pas de fonctionnalités avancées. Il est idéal pour les petites entreprises, les artisans, les professions libérales, les associations, les artistes, etc.",
      delai: "Délai de lancement: En règle général, le délai de création et lancement est compris entre 2 et 4 semaines, selon la complexité du projet",
      tarif:
        "Tarif: À partir de 1500 euros.",
    },
    {
      type: "Site E-Commerce",
      description:
        "Le E-commerce vous permet de vendre vos produits 24/7. C'est une hyper présence en ligne nécessitant un travail soigneux aussi bien dans la gestion du front-end, comme sur la partie back-end et notamment sur la sécurité au niveau de la gestion des stocks et des paiements.",
      delai:
        "Délai de lancement: En règle général, le délai de lancement est au minimum de 4 semaines, ce délai peut se rallonger selon la complexité du projet",
      tarif:
        "Tarif: À partir de 2500 euros.",
    },
    {
      type: "Blog",
      description: "Un Blog vous permet de créer et de poster des articles et d'ouvrir ces posts à des retours de commentaires de vos utilisateurs. Idéal pour obtenir des prospects et les convertir. Idéal pour les entreprises qui souhaitent partager leur expertise, leur actualité, leur veille, etc.",
      delai:
        "Délai de lancement: En règle général, le délai de lancement est de 2 semaines. Le blog peut également être ajouté à un autre type de site.",
      tarif:
        "Tarif:  À partir de 500 euros pour un simple Blog",
    },
    {
      type: "Portfolio",
      description: "Un Portfolio est idéal pour les artistes, les photographes, les graphistes, les designers, les architectes, les créateurs, les illustrateurs, les musiciens, les écrivains, etc. Il permet de présenter vos réalisations, vos créations, vos projets, vos oeuvres, etc.",
      delai:
        "Délai de lancement: En règle général, le délai de lancement débute autour de 4 semaines, ce délai peut se rallonger selon la complexité du projet",
      tarif:
        "Tarif: À partir de 1500 euros.",
    },
    {
      type: "Site Corporate",
      description: "Un site Corporate vous permet de présenter votre entreprise, vos services, vos produits, vos valeurs, votre équipe, vos actualités, etc. Il est idéal pour les entreprises, les PME, les TPE, les grandes entreprises, les multinationales, etc.",
      delai: "Délai de lancement: En règle général, le délai de lancement débute autour de 4 semaines, ce délai peut se rallonger selon la complexite du projet",
      tarif:
        "Tarif: À partir de 2000 euros.",
    },
    {
      type: "Site Institutionnel",
      description: "Un site institutionnel vous permet de présenter votre institution, vos services, vos produits, vos valeurs, votre équipe, vos actualités, etc. Il est idéal pour les institutions, les écoles, les universités, les collectivités, les mairies, les associations, les ONG, etc.",
      delai: "Délai de lancement: En règle général, le délai de lancement débute autour de 4 semaines, ce délai peut se rallong",
      tarif:
        "Tarif: À partir de 2000 euros.",
    },
  ];
</script>

<Header />

<section class="sites-section" in:fade={{ duration: 1000 }}>
  <div class="hero">
    <img src={imgHero} alt="" class="imgHero" />
    <h1>Création de <br /><span>Site Web</span></h1>
    <h3>
      Grâce à notre expertise dans la création de sites Internets, nous mettons en oeuvre notre savoir-faire pour...
    </h3>
    <div class="wrapper-contact">
      <a class="contact" href="/#footer">Nous contacter</a>
      <a class="contact2" href="/#footer">Devis gratuit</a>
    </div>
  </div>

  <Profits />

  <div class="section-slider">
    <h1>Nous maîtrisons la conception de tous les types de site Internet.</h1>
    <h3>Découvrez les différents types de sites internet, nos délais de lancement et nos tarifs.</h3>
    <div class="container-slider">
      <div class="wrapper-slider">
        {#each sitesTab as site}
          <CardsSites type={site.type} description={site.description} delai={site.delai} tarif={site.tarif} />
        {/each}
      </div>
    </div>
  </div>
  <FSection />

  <div class="wrapper-conclusion">
    <h4>
      Vous souhaitez en savoir d'avantage ou nous parlez de votre projet? <br />Nous sommes là pour vous écouter et vous
      apporter toutes nos solutions. <br /><br />On en parle autour d'un café ?
    </h4>
    <div class="wrapper-contactez">
      <a href="mailto:gralypho@gmail.com " class="contact"><i class="fa-regular fa-envelope"></i></a>
      <a href="tel:0672901614" class="contact"><i class="fa-solid fa-phone-volume"></i></a>
      <a href="tel:0672901614" class="contact"><i class="fa-solid fa-mug-hot"></i></a>
    </div>
  </div>
</section>

<!-- <div class="wrapper-text-intro">
  <h1>
    Votre futur site internet est un outil. Et cet outil doit vous servir à atteindre votre objectifs. Qu'il s'agisse
    d'atteindre vos clients, de vendre vos produits, de proposer vos services, de communiquer, de toucher vos prospects,
    de développer votre activité, votre rayonnement, votre notoriété (...), tout cela repose sur trois piliers: Un
    design réussi, un contenu pertinent, un référencement optimisé
  </h1>
</div> -->

<style>
  .sites-section {
    display: grid;
    grid-template-columns: repeat(12, 1fr);
    grid-template-rows: auto;
    background-color: rgb(245, 244, 244);
    height: auto;
    font-size: 16px;
  }
  .hero {
    grid-column: 1/13;
    grid-row: 1;
    display: flex;
    flex-direction: column;
    align-items: center;
    justify-content: center;
    height: auto;
    background-color: var(--primary);
  }
  .hero h1 {
    text-align: center;
    font-family: Epilogue;
    font-weight: 900;
    font-size: var(--xlhero);
    color: rgb(255, 255, 255);
    margin-top: 0px;
    letter-spacing: -1px;
    padding: 0px;
    line-height: 50px;
    margin-top: 50px;
  }
  .hero h1 span {
    color: yellow;
  }
  .hero h3 {
    font-family: poppins;
    font-weight: 300;
    font-size: var(--m);
    color: rgb(224, 222, 222);
    text-align: center;
  }
  .imgHero {
    width: 50%;
    height: 50%;
    margin-top: 30px;
  }
  .wrapper-contact{
    display: flex;
    gap: 0px;
    margin: 40 auto;
    margin-bottom: 40px;
  }
  .contact {
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
  .contact2 {
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
  .contact:hover {
    animation: bounce 0.4s ease-in-out;
  }
  .contact2:hover {
    animation: bounce 0.4s ease-in-out;
  }

  .container-slider {
    overflow-x: auto;
    margin-left: 0px;
    border-right: 3px double var(--primary);
    width: 100vw;
  }
  .wrapper-slider {
    display: flex;
    flex-direction: row;
    flex-wrap: nowrap;
    border-radius: 20px;
    justify-content: start;
    align-items: center;
    margin-bottom: 30px;
    gap: 20px;
  }
  .section-slider {
    grid-column: 1/12;
    grid-row: 3;
    margin-top: 50px;
    margin-left: 20px;
  }
  .section-slider h1 {
    text-align: left;
    font-family: epilogue;
    font-size: var(--xl);
    font-weight: 700;
    color: var(--primary);
    margin-top: 20px;
    letter-spacing: -3px;
  }
  .section-slider h3 {
    text-align: left;
    font-family: poppins;
    font-weight: 300;
    font-size: var(--m);
    color: grey;
    margin-top: 20px;
    margin-bottom: 50px;
  }

  .wrapper-conclusion {
    grid-column: 2/12;
    grid-row: 6;
    display: flex;
    flex-direction: column;
    justify-content: center;
    align-items: center;
    margin-top: 50px;
  }
  h4 {
    z-index: 2;
    margin-top: 30px;
    color: grey;
    text-align: left;
    line-height: 30px;
    font-weight: 600;
    font-size: 1.2em;
    font-family: poppins;
    text-align: center;
  }
  a {
    padding: 20px;
    border-radius: 10px;
    font-size: 2em;
    color: white;
    background-color: var(--CTA);
    z-index: 2;
    box-shadow: 0px 0px 10px 0px #0000004d;
  }
  a:hover {
    animation: bounce 0.4s ease-in-out;
  }
  .wrapper-contactez {
    display: flex;
    gap: 20px;
    margin-top: 20px;
    align-items: center;
    justify-content: center;
    margin-bottom: 40px;
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

  @media screen and (min-width: 1224px) and (max-width: 2500px) {
    .hero h1 {
      line-height: 130px;
    }
    .hero h3 {
      line-height: 30px;
      font-size: 1.2em;
      margin-top: 30px;
      margin-bottom: 50px;
      width: 60%;
    }
    .contact,
    .contact2 {
      font-size: 1.3em;
      width: auto;
    }
  }
  @media screen and (min-width: 768px) and (max-width: 1224px) {
    .hero h1 {
      line-height: 70px;
    }
    .hero h3 {
      line-height: 30px;
      font-size: 1em;
      margin-top: 30px;
      margin-bottom: 50px;
      width: 60%;
    }
      .contact,
    .contact2 {
      font-size: 1em;
    }
  
    .section-slider h1 {
      line-height: 55px;
      letter-spacing: -2px;
    }
  }
  @media screen and (min-width: 300px) and (max-width: 768px) {
    .imgHero {
      width: 110%;
      height: 110%;
      margin-top: 50px;
      margin-right: 20px;
    }
    .hero h1 {
      line-height: 50px;
      font-size: 3.1em;
    }
    .hero h3 {
      line-height: 30px;
      font-size: 1em;
      margin-top: 30px;
      margin-bottom: 50px;
      width: 60%;
    }
    .section-slider h1 {
      line-height: 40px;
      letter-spacing: -1px;
    }
    .contact,
    .contact2 {
      font-size: 1em;
    }
  }
</style>
