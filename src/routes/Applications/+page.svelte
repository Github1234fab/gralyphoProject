<script>
  import { fade, slide } from "svelte/transition";
  // import bg from "../../Assets/png-gralypho/41.png";
  import Header from "../../sections/Header.svelte";
</script>

<Header />
<section class="application-section" in:fade={{ duration: 3000 }}>

<div class="wrapper-testimonial">
<h2>"La seule limite à ce que vous pouvez réaliser est celle que vous imaginez." </h2>
<h3>Roy T. Bennett</h3>
</div>


Tout à chacun peut effectivement réaliser un site internet en quelques clics, mais qu'en est-il
    sous le capot? Et qu'en est-il en matière de SEO pour votre référencement? Du point de vue de l'UX et de l'UI,
    est-ce que la navigation de votre site est facile, compréhensible, intuitive? Est-ce que vos fonctionnalité sont
    sécurisées? Est-ce que votre conception respecte les normes imposées par le W3C? <br /><br />
    Nous sommes passionnés par le Web et par la création d'outils digitaux. Un site internet ou une application sont censés
    améliorer et faciliter la vie d'un utilisateur. Ce sont de véritable outils qui permettent d'obtenir un gain de temps
    et un gain de productivité. Pendant que vous travailler à autre chose ou que vous vous occupez de votre vie sociale et
    personnelle, votre outil travaille pour vous sur le Web, avec une hyper présence. Une site E-commerce est ouvert 24/7
    et mis à part l'envoi du produit, aucun travaux ne sont nécessaires. <br /> <br /> Une Visibilité accrue sur le web nourrie
    par un exellent référencement, vous permet de trouver des prospects et de les convertir en clients. <br /> Une
    application ouvre les portes d'une infiinité de solutions pour tout utilisateurs et dans tous les domaines et même
    si ne nombreuses application existent déjà, les possibilités de création sont énormes car le monde évolue et les
    besoins des utilisateurs sont toujours naissants. <br /><br>










</section>

<style>
.application-section {
 display:grid;
  grid-template-columns: repeat(12, 1fr);
  grid-template-rows: auto;
  height: auto;
  font-size: 16px;

  } 

  
  .wrapper-testimonial {
    display: flex;
    justify-content: center;
    align-items: center;
    flex-direction: column;
    margin-top: 50px;
    margin-bottom: 50px;
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
 

@media screen and (min-width: 1400px) and (max-width: 2500px){


}

@media screen and (min-width: 1200px) and (max-width: 1400px){


}


@media screen and (min-width: 992px) and (max-width: 1200px){


}

@media screen and (min-width: 768px) and (max-width: 992px){


}

@media screen and (min-width: 576px) and (max-width: 767px){


}

@media screen and (min-width: 300px) and (max-width: 575px){


}


</style>
