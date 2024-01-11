<script>
  import Robot from "../Assets/png-gralypho/Saly-39.png";
  import { onMount } from "svelte";
  import triangle from "../Assets/png-gralypho/nnneon (6).svg";
  import TypeSiteCards from "../Components/TypeSiteCards.svelte";
  import vitrine from "../Assets/png-gralypho/store-solid.svg"
  import  portfolio from '../Assets/png-gralypho/address-card-regular.svg';
  import commerce from '../Assets/png-gralypho/euro-sign-solid.svg';
  import blog from '../Assets/png-gralypho/blog-solid.svg';
  import corporate from '../Assets/png-gralypho/user-tie-solid.svg';
  import  institution from '../Assets/png-gralypho/building-columns-solid.svg';

  let SiteCards = [
    {
      title: "Site vitrine",
      icon: vitrine,
      p: "Un site vitrine est un site web qui présente l'activité d'une entreprise ou d'une organisation. Il a pour objectif de présenter les produits et services de l'entreprise et de donner aux visiteurs toutes les informations nécessaires pour les inciter à contacter l'entreprise.",
    },
    {
      title: "Site e-commerce",
      icon: commerce,
      p: "Un site e-commerce est un site web qui permet de vendre des produits ou des services en ligne. Il a pour objectif de présenter les produits et services de l'entreprise et de donner aux visiteurs toutes les informations nécessaires pour les inciter à contacter l'entreprise.",
    },
    {
      title: "Blog",
      icon: blog,
      p: "Un site sur mesure est un site web qui présente l'activité d'une entreprise ou d'une organisation. Il a pour objectif de présenter les produits et services de l'entreprise et de donner aux visiteurs toutes les informations nécessaires pour les inciter à contacter l'entreprise.",
    },
    {
      title: "Portfolio",
      icon: portfolio,
      p: "Un site vitrine est un site web qui présente l'activité d'une entreprise ou d'une organisation. Il a pour objectif de présenter les produits et services de l'entreprise et de donner aux visiteurs toutes les informations nécessaires pour les inciter à contacter l'entreprise.",
    },
    {
      title: "Corporate",
      icon: corporate,
      p: "Un site e-commerce est un site web qui permet de vendre des produits ou des services en ligne. Il a pour objectif de présenter les produits et services de l'entreprise et de donner aux visiteurs toutes les informations nécessaires pour les inciter à contacter l'entreprise.",
    },
    {
      title: "Insitutionnel",
      icon: institution,
      p: "Un site sur mesure est un site web qui présente l'activité d'une entreprise ou d'une organisation. Il a pour",
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
  <!-- <img src={Robot} alt="icon de robot en 3D" class="robot gsap" />
  <img src={triangle} alt="icon de robot en 3D" class="triangle gsap" /> -->
  <h1>Grâce à nos solutions digitales  <span>100%</span> sur mesure, obtenez le site Web qui vous convient !</h1>

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
    /* background: radial-gradient(circle at top, var(--colorO), var(--colorN)); */
    background-size: 100% 100%;
   /* margin-left: 30px;
    margin-right: 30px;
    border-radius: 6px;
    margin-top: 0px;
    opacity: 0.2; */
  }
  .C-section h1 {
    grid-column: 2/12;
    grid-row: 2;
    font-size: 2.4em;
    font-weight: 800;
    text-align: left;
    color: var(--colorC);
    margin-top: 50px;
  }

    .C-section h1 span {
    font-weight: 800;
    color: transparent;
    -webkit-background-image: inear-gradient(to left, var(--colorD), var(--colorI));
    background-image: linear-gradient(to left, var(--colorD), var(--colorI));
    -webkit-background-clip: text;
    background-clip: text;
  }
 
  /* .robot {
    transform: scale(0.6);
    height: 150px;
    width: 150px;
    margin-top: 50px;
    z-index: 2;
    grid-column: 6;
    grid-row: 1;
  }
  .triangle {
    transform: scale(0.2);
    height: 150px;
    z-index: 1;
    align-self: center;
       grid-column: 6;
          grid-row: 1;
  }
  .gsap {
    opacity: 1;
  } */
    .wrapper-cards {
 grid-column: 2/12;
    grid-row: 3;
    margin-top: 100px;
    display: flex;
    flex-wrap: wrap;
    align-items: center;
    justify-content: center;
    gap: 30px;

  }

  @media screen and (max-width: 768px) {
    .C-section {
      font-size: 13px;
    }
 
  }
</style>
