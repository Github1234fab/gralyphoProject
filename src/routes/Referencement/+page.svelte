<script>
  import { fade, slide } from "svelte/transition";
  // import bg from "../../Assets/png-gralypho/41.png";
  import Header from "../../sections/Header.svelte";
</script>

<Header />
<section class="" in:fade={{ duration: 3000 }}>
  <div class="wrapper">
    <h1>Référencement.</h1>
    <!-- <img src={bg} alt="" class="bg" /> -->

    <p>
     <span><strong>SEO</strong> ou <strong>SEA</strong> lequel choisir?! </span><br><br> 
 C'est le nerf de la guerre, évidemment !<br> <br>
      C'est le but de tout à chacun, être référencé en première page des moteurs de recherche. Être visible et accessible. <br> <br>Comment réaliser cela? Comment faire pour que nos prospects, nos clients, nos utilisateurs nous trouvent, rapidement, facilement? Tout en encore une question de stratégie allant du choix de votre nom de domaine, aux mots clefs utilisés pour votre référencement,  en passant par la qualité du copywriting et votre stratégie à court et long terme. <br><br>
    Mais, il y a deux techniques principales dans le domaine du référencement. La technique naturelle et la technique payante.  <br>La technique de référencement naturel, c'est  ce que l'on appelle le SEO (Search Engine Optimization)  et la technique payante, le SEA (search engine advertising). <br><br>Le référencement naturel requiert de l'expérience en rédaction de contenu web (copywriting), mais également de très bonnes connaissances en accessibilité et des normes imposées notamment par le W3C. Par accessibilité on entend, accessible à toute personne présentant un handicap. Qu'il soit visuel, cognitif, physique ou neurologique. Un texte pas assez contrasté, une animation trop intense pouvant provoquer l'épillepsie, une image non décrite pour les non-voyants, etc. <br>Les normes imposées par le W3C pèsent maintenant considérablement sur le référencement naturel, car le robot Google prend maintenant en compte ces paramètres d'accessibilité du Web. <br><br>
  Quant au référencement payant, le SEA, il requiert de très bbonnes connaissances en matière d'outil de promotion marketing.  <br>Il s'agit de campagne de publicité qui peuvent soient être diffusés sur des sites partenaires soient en haut de page des moteurs de recherche, ou les deux.  <br><br>Ces outils d'apprence assez simples sont en réalité très complexe. Chaque mot clef est payant, une stratégie est donc nécessaire en amont. La qualité de la rédaction de l'annonce doit être pertinente et s'adresser facilement et directement au coeur de cible. Les annonces peuvent être automatisées et se déclencher à des périodes déterminées.  
    </p>

    <h4>
      Vous souhaitez aborder la question du référencement?  <br>Nous sommes là pour vous écouter et vous apporter toutes nos solutions!
    </h4>
    <div class="wrapper-contact">
      <a href="mailto:gralypho@gmail.com " class="contact"><i class="fa-regular fa-envelope"></i></a>
      <a href="tel:0672901614" class="contact"><i class="fa-solid fa-phone-volume"></i></a>

    </div>
  </div>
</section>

<style>
  .wrapper-contact {
    display: flex;
    gap: 30px;
    justify-content: center;
    align-items: center;
    margin-top: 50px;
  }
  h4 {
    z-index: 2;
    margin-top: 30px;
    color: var(--colorC);
    text-align: left;
    line-height: 30px;
    font-weight: 600;
    font-size: 1.2em;
    font-family: epilogue;
    text-align: center;
  }
  a {
    border: 2px solid var(--blue);
    padding: 20px;
    border-radius: 10px;
    font-size: 2em;
    color: var(--colorC);
    z-index: 2;
  }
  a:hover {
    animation: bounce 0.4s ease-in-out;
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
  section {
    display: grid;
    grid-template-columns: repeat(12, 1fr);
    grid-template-rows: auto;
    /* background-color: var(--colorO); */
    height: 100%;
    width: 100%;
    margin-top: 30px;
    margin-bottom: 50px;
  }
  .wrapper {
    grid-column: 1/13;
    grid-row: 1;
    display: flex;
    flex-direction: column;
    justify-content: left;
    align-items: left;
    height: 100%;
    position: relative;
    padding: 30px;
  }
  .wrapper::after {
    position: absolute;
    content: "";
    background-color: #1a1c2186;
    top: 0;
    left: 0;
    right: 0;
    bottom: 0;
  }
  section h1 {
    z-index: 2;
    text-align: left;
    font-family: Kanit;
    font-weight: 900;
    font-size: 2.7em;
    color: white;
    margin-top: 50px;
    line-height: 37px;
  }
  section p span {
    z-index: 2;
    color: white;
    font-size: 1.5rem;
    font-weight: 600;
    text-align: left;
    line-height: 30px;
    margin-top: 30px;
    font-family: kanit;
  }
  section p {
    z-index: 2;
    margin-top: 30px;
    color: var(--colorC);
    text-align: left;
    line-height: 30px;
    font-weight: 300;
    font-size: 1.2em;
    font-family: epilogue;
  }
  /* .bg {
    z-index: 2;
    margin-top: 30px;
    border-radius: 20px;
    height: 300px;
    width: 300px;
  } */
  /* ol {
    z-index: 2;
    color: var(--colorC);
    text-align: left;
    line-height: 30px;
    font-weight: 300;
    font-size: 1.2em;
    font-family: epilogue;
  } */
</style>
