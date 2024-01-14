<script>
  import Robot from "../Assets/png-gralypho/Saly-39.png";
  import { onMount } from "svelte";
  import triangle from "../Assets/png-gralypho/nnneon (6).svg";
  import TypeSiteCards from "../Components/TypeSiteCards.svelte";
  import vitrine from "../Assets/png-gralypho/store-solid.svg";
  import portfolio from "../Assets/png-gralypho/address-card-regular.svg";
  import commerce from "../Assets/png-gralypho/euro-sign-solid.svg";
  import blog from "../Assets/png-gralypho/blog-solid.svg";
  import corporate from "../Assets/png-gralypho/user-tie-solid.svg";
  import institution from "../Assets/png-gralypho/building-columns-solid.svg";

  let SiteCards = [
    {
      title: "Site vitrine",
      icon: vitrine,
      p: "Créer un site internet vitrine permet de présenter la société, ses produits et ses services. Il permet de fournir des informations aux clients potentiels et de les diriger vers les canaux de vente de l’entreprise..",
    },
    {
      title: "Site e-commerce",
      icon: commerce,
      p: "Réaliser un site internet e-commerce permet à une entreprise de vendre des produits, des contenus ou des services en ligne 24h/24. Les fonctionnalités clés d’un site e-commerce comprennent :...",
    },
    {
      title: "Blog",
      icon: blog,
      p: "Le blog d’entreprise est un site éditorial animé par un ou plusieurs auteurs qui publient des articles et des contenus sur des sujets spécifiques B2C ou B2B. ",
    },
    {
      title: "Portfolio",
      icon: portfolio,
      p: "Le portfolio est une plateforme internet professionnelle qui permet aux créatifs de présenter leurs travaux et leurs réalisations. ",
    },
    {
      title: "Corporate",
      icon: corporate,
      p: "Les grandes entreprises, institutions ou organisations ont besoin de présenter leurs activités. Un site web corporate apporte les réponses nécessaires de ce point de vue.",
    },
    {
      title: "Insitutionnel",
      icon: institution,
      p: "Le site institutionnel est destiné à promouvoir l’image d’une organisation telle que les établissements d’enseignement, les associations et les organismes à but non lucratif. ",
    },
  ];

  onMount(() => {
    gsap.to(".gsap", {
      scale: 1,
      ease: "expoScale",
      scrollTrigger: {
        trigger: ".gsap",
        start: "top 700px",
        end: "-200px",
        scrub: 1,
      },
    });
    gsap.to(".C-section", {
      opacity: 1,
      ease: "expoScale",
      scrollTrigger: {
        trigger: ".C-section",
        start: "top 500px",
        end: "-200px",
        scrub: 1,
      },
    });
  });
</script>

<section class="C-section" id="sectionC">
  <h1>Avec Gralypho, le futur de votre business commence maintenant.</h1>
  <h2> Vous avez besoin d'un site Internet? Découvrez toutes nos solutions de sites Web et choisissez celui dont vous avez besoin !</h2>

  <div class="wrapper-cards">
    {#each SiteCards as Cards}
      <TypeSiteCards title={Cards.title} icon={Cards.icon} p={Cards.p} />
    {/each}
  </div>
</section>

<style>
  .C-section {
    display: grid;
    grid-template-columns: repeat(12, 1fr);
    grid-template-rows: 1;
    height: auto;
    font-size: 16px;
  }
  .C-section h1 {
    grid-column: 2/12;
    grid-row: 2;
    font-size: 2.7em;
    font-weight: 900;
    text-align: left;
    color: var(--colorC);
    margin-top: 50px;
  }
   .C-section h2 {
    grid-column: 2/12;
    grid-row: 2;
    font-size: 1.2em;
    font-weight: 300;
    text-align: left;
    color: white;
    margin-top: 180px;
  }



  .wrapper-cards {
    grid-column: 2/12;
    grid-row: 3;
    margin-top: 100px;
    display: flex;
    flex-wrap: wrap;
    align-items: center;
    justify-content: center;
    gap: 50px;
    margin-bottom: 100px;
  }

  @media screen and (max-width: 768px) {
    .C-section {
      font-size: 16px;
    }
    .wrapper-cards {
      margin-top: 65px;
    }
  }
</style>
