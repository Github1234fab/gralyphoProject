<script>
  import World from "../Assets/png-gralypho/Saly-12.png";
  import Analist from "../Assets/png-gralypho/Saly-44.png";
  import { onMount } from "svelte";
   import six from "../Assets/png-gralypho/six.svg";

  onMount(() => {
    gsap.to(".smartphone", {
      rotate: 740,
      scale: 1,
      scrollTrigger: {
        trigger: ".smartphone",
        start: "top 700px",
        end: "-300px",
        scrub: 2,
      },
    });
  });
</script>

<section class="F-section" id="sectionF">
  <div class="wrapper-text">
    <img src={World} alt="" class="smartphone gsap3" />
    <img src={six} alt="" class="six gsap3" />
    <h1>Rérencement: <strong>SEO</strong> ou <strong>SEA</strong>?! <br> Profitez de notre expérience en référencement naturel ou payant.</h1>
    <h2>C'est le nerf de la guerre, évidemment !<br> 
      C'est le but de tout à chacun, être référencé en première page des moteurs de recherche. Être visible et accessible. <br> <br>Comment réaliser cela? Comment faire pour que nos prospects, nos clients, nos utilisateurs nous trouvent, rapidement, facilement? Tout en encore une question de stratégie allant du choix de votre nom de domaine, aux mots clefs utilisés pour votre référencement,  en passant par la qualité du copywriting et votre stratégie à court et long terme. <br><br>
    Mais, il y a deux techniques principales dans le domaine du référencement. La technique naturelle et la technique payante.  <br>La technique de référencement naturel, c'est  ce que l'on appelle le SEO (Search Engine Optimization)  et la technique payante, le SEA (search engine advertising). <br><br>Le référencement naturel requiert de l'expérience en rédaction de contenu web (copywriting), mais également de très bonnes connaissances en accessibilité et des normes imposées notamment par le W3C. Par accessibilité on entend, accessible à toute personne présentant un handicap. Qu'il soit visuel, cognitif, physique ou neurologique. Un texte pas assez contrasté, une animation trop intense pouvant provoquer l'épillepsie, une image non décrite pour les non-voyants, etc. <br>Les normes imposées par le W3C pèsent maintenant considérablement sur le référencement naturel, car le robot Google prend maintenant en compte ces paramètres d'accessibilité du Web. <br><br>
  Quant au référencement payant, le SEA, il requiert de très bbonnes connaissances en matière d'outil de promotion marketing.  <br>Il s'agit de campagne de publicité qui peuvent soient être diffusés sur des sites partenaires soient en haut de page des moteurs de recherche, ou les deux.  <br><br>Ces outils d'apprence assez simples sont en réalité très complexe. Chaque mot clef est payant, une stratégie est donc nécessaire en amont. La qualité de la rédaction de l'annonce doit être pertinente et s'adresser facilement et directement au coeur de cible. Les annonces peuvent être automatisées et se déclencher à des périodes déterminées.  </h2>
  </div>
</section>

<style>
  .F-section {
    scroll-margin-top: -50px;
    display: grid;
    grid-template-columns: repeat(12, 1fr);
    grid-template-rows: auto;
    height: auto;
    font-size: 16px;
    background-color: var(--colorO);
    margin-top: 170px;
    margin-bottom: 100px;
  }
  .wrapper-text {
    grid-column: 2/12;
    grid-row: 2;
    border-radius: 20px;
    padding: 20px;
    display: flex;
    flex-direction: column;
        /* border: solid 1px rgb(55, 55, 55); */
     /* background-image: url(../Assets/png-gralypho/tttwinkle.svg); */
    background-repeat: no-repeat;
    background-position: top;
    background-size: 50%;
  }
  .F-section h1 {
    word-wrap: break-word;
    grid-column: 2/12;
    text-align: left;
    grid-row: 2;
    font-family: epilogue;
    font-weight: 500;
    font-size: 1.7em;
    color: white;
    margin-top: 50px;
    padding: 10px;
    line-height: 37px;
  }
  .F-section h2 {
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
  .smartphone {
    height: 200px;
    margin-top: 0px;
    transform: rotate(20deg);
    z-index: 2;
    align-self: center;
    margin-top: 50px;
  }
  .six {
    height: 200px;
    margin-top: -190px;
    transform: rotate(20deg);
    z-index: 1;
    align-self: center;
  }

    @media screen and (max-width: 768px) {
    .F-section {
      font-size: 13px;
    }
        .wrapper-text{
      background-size: 100%;
    }
  }
</style>
