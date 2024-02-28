<script>
  import { fade, slide } from "svelte/transition";
  // import bg from "../../Assets/png-gralypho/41.png";
  import Header from "../../sections/Header.svelte";
</script>

<Header />
<section class="" in:fade={{ duration: 3000 }}>
  <div class="wrapper background-repeat">
    <h1>Développement et intégration de composant.</h1>
    <!-- <img src={bg} alt="" class="bg" /> -->

    <p>
      <span>C'est quoi, un composant ?!</span> <br /><br />
      Dans le monde en constante évolution du développement web, les composants jouent un rôle essentiel pour créer des sites
      internet à la pointe de la technologie, répondant aux besoins spécifiques de nos clients. Imaginez avoir une horloge
      élégante intégrée à votre site, offrant une expérience visuelle captivante tout en informant vos visiteurs du temps
      qui s'écoule. Un composant web c'est ça, un élément que l'on ajoute à votre site ou votre application pour répondre
      à de nouveaux besoins.<br /><br />

      <span>Un composant pour répondre à quels besoins ?</span> <br /><br />
      Besoin d'une fonction de prise de rendez-vous fluide et conviviale ? Nos composants sont conçus pour faciliter l'interaction
      avec vos clients, en leur permettant de planifier des rendez-vous en ligne de manière transparente. Vous pourriez également
      intégrer une fonction météo pour informer vos visiteurs des conditions actuelles, ajoutant ainsi une touche pratique
      et engageante à votre site. <br /><br />

      Si votre vision inclut des animations de contenu pour rendre votre site dynamique et attrayant, nos composants
      peuvent également répondre à cette demande. Des animations subtiles aux effets visuels saisissants, nous
      personnalisons chaque composant pour refléter l'identité unique de votre entreprise. <br /><br />

      Avec notre approche axée sur les composants, nous façonnons des sites web interactifs et fonctionnels, anticipant
      et répondant à vos besoins spécifiques. Ensemble, créons un site internet qui va au-delà des attentes, offrant une
      expérience en ligne exceptionnelle à vos visiteurs."<br /><br />
    </p>

    <h4>
      Vous souhaitez en savoir plus sur les composants ? <br />Alors parlez nous de votre projet, autour d'un café!
    </h4>
    <div class="wrapper-contact">
      <a href="mailto:gralypho@gmail.com " class="contact"><i class="fa-regular fa-envelope"></i></a>
      <a href="tel:0672901614" class="contact"><i class="fa-solid fa-phone-volume"></i></a>
      <a href="tel:0672901614" class="contact"><i class="fa-solid fa-mug-hot"></i></a>
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
    font-weight: 400;
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
    font-weight: 600;
    font-size: var(--xl);
    color: white;
    margin-top: 50px;
    line-height: 37px;
  }
  section p span {
    z-index: 2;
    color: white;
    font-size: var(--l);
    font-weight: 400;
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
    font-size: var(--m);
    font-family: epilogue;
  }


</style>
