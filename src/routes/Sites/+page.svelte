<script>
  import { fade, slide } from "svelte/transition";
  // import bg from "../../Assets/png-gralypho/41.png";
  import Header from "../../sections/Header.svelte";
</script>

<Header />
<section class="" in:fade={{ duration: 3000 }}>
  <div class="wrapper">
    <h1>Sites Web</h1>
    <!-- <img src={bg} alt="" class="bg" /> -->
    <p>
      Gralypho, votre partenaire digital, réinvente votre business en proposant des sites web sur mesure. Notre approche
      stratégique allie design innovant, fonctionnalités avancées et expérience utilisateur exceptionnelle. De la
      conception web à la stratégie marketing, nous façonnons des sites qui captivent, convertissent et propulsent votre
      présence en ligne vers de nouveaux sommets. Choisissez Gralypho pour un site web qui va au-delà de l'esthétique,
      créant des expériences en ligne alignées sur vos objectifs commerciaux. <br /><br />
      <span>Quelle est la durée estimée pour la création et la livraison de votre site web ?</span> <br /><br />
      <li>
        La durée de création et de livraison de votre site web dépend de la complexité de votre projet. <br />
        S'il s'agit d'un site vitrine simple, sans base de données, ni gestion complexe, le délai de création et de livraison
        peut être compris entre 2 et 3 semaines.
      </li>
      <br /><br />
      <li>
        Pour un site e-commerce avec des bases de données et des gestions complexes, le délai de création et de
        livraison peut être compris entre 1 et 3 mois.
      </li>
      <br /><br />
      <li>
        Concernant les autres types de sites Portfolio, Corporate, institutionnel et Blog tout dépend du projet, de son
        exigence en Design, en UI et UX, en contenu et gestion de données.
      </li>
      <br /><br />
      <span>Quel est le tarif pour un site internet ?</span> <br /><br />
      Les tarifs peuvent se situer entre 1000€ et 10 000€ euros. <br /><br />
      Ce budget variera en fonction du nombre de pages, de fonctionnalité de gestion des stocks, de base de données, de paiement,
      de gestion de planning (...). <br /><br />
      <span>Comment se déroule la création de votre site internet?</span> <br /><br />
    </p>
    <ol>
      <li>Nous vous posons de nombreuses questions ciblées sur votre projet afin d'en comprendre la finalité.</li>
      <br />
      <li>Nous vous écoutons, activement.</li>
      <br />
      <li>Nous vous proposons généralement trois maquettes différentes et vous laissons choisir parmis celles-ci .</li>
      <br />
      <li>Vous avez tout le loisir à cette étape de modifier les éléments présentées dans la maquette.</li>
      <br />
      <li>
        Une fois les éléments fixés, nous enclenchons l'intégration, c'est à dire que les éléments de la maquette
        deviennent du code informatique, permettant notamment l'affichage des pages de votre site sur le web.
      </li>
      <br />
      <li>
        Ensuite, votre site est intégré en version bêta, et fera l'objet de plusieurs tests de compatiblité sur les
        différents navigateurs et différents test utilisateurs.
      </li>
      <br />
      <li>Lorsque votre site internet a passé les différents tests, il vous est enfin livré! 🍾.🍾.🍾.</li>
      <br />
    </ol>
    <h4>Vous souhaitez en savoir d'avantage ou nous parlez de votre projet?  <br>Nous sommes là pour vous écouter et vous apporter toutes nos solutions. <br><br>On en parle autour d'un café ?</h4>
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
    word-wrap: break-word;
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
  ol {
    z-index: 2;
    color: var(--colorC);
    text-align: left;
    line-height: 30px;
    font-weight: 300;
    font-size: 1.2em;
    font-family: epilogue;
  }
</style>
