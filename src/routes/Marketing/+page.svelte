<script>
  import { fade, slide } from "svelte/transition";
  // import bg from "../../Assets/png-gralypho/41.png";
  import Header from "../../sections/Header.svelte";
</script>

<Header />
<section class="" in:fade={{ duration: 3000 }}>
  <div class="wrapper">
    <h1>Marketing Digital & conseil</h1>
    <!-- <img src={bg} alt="" class="bg" /> -->

    <p>
     <span>Marketing Digital, pour quelle utilité ?<br><br> </span>

Dans l'ère numérique d'aujourd'hui, le marketing digital est la clé du succès commercial. Chez Gralypho, nous comprenons l'importance cruciale de créer une présence en ligne forte et impactante pour propulser votre entreprise vers de nouveaux sommets. <br><br>
  <span>Visibilité et public cible.<br><br> </span>
Notre équipe spécialisée en marketing digital est déterminée à maximiser la visibilité de votre marque, attirer un public ciblé et stimuler la croissance de votre entreprise. Du référencement (SEO) pour garantir que votre site soit trouvé par ceux qui recherchent vos produits ou services, aux campagnes publicitaires percutantes sur les médias sociaux, nous concevons des stratégies sur mesure pour répondre à vos objectifs commerciaux. <br><br>

  <span>Rôle des médias Sociaux.<br><br> </span>
Nous exploitons la puissance des médias sociaux pour créer des connexions authentiques avec votre audience, stimuler l'engagement et renforcer la notoriété de votre marque. Nos experts en marketing digital sont également experts dans la gestion de campagnes publicitaires en ligne, optimisant chaque euro dépensé pour assurer un retour sur investissement. <br><br>
  <span>Marketing Digital pour propulser votre entreprise vers le succès.<br><br> </span>
Le marketing digital va au-delà de la simple visibilité en ligne ; c'est un moyen efficace de créer des relations durables avec vos clients. Grâce à notre approche créative et axée sur les résultats, nous sommes prêts à transformer votre présence en ligne en une force motrice qui propulse votre entreprise vers de nouveaux horizons. Découvrez comment le marketing digital peut propulser votre entreprise vers le succès. <br><br>
    </p>

    <h4>
      Nous sommes là pour répondre à toutes vos questions et vous proposer toutes nos solutions autour d'un petit café!
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
