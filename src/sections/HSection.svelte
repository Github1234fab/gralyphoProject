<script>
  import Climber from "../Assets/png-gralypho/Saly-15.png";
  import six from "../Assets/png-gralypho/six.svg";
  import Header from "../sections/Header.svelte";

  import { onMount } from "svelte";

  onMount(() => {
    gsap.to(".gsap5", {
      rotation: 730,
      duration: 2,
      scrub: 3,
    });
  });

</script>

<Header />
<section class="H-section">
  <div class="wrapper-png">
    <img src={Climber} alt="" class="climb gsap5" />
    <img src={six} alt="" class="six gsap5" />
  </div>
  <div class="wrapper-text">
    <h1><span>Gralypho</span>. Expertise et Expérience, votre victoire Digitale assurée !</h1>
  </div>
  <div class="wrapper-contact">
    <!-- <h5>Contactez-nous</h5> -->
    <div class="wrapper-media-contact">
      <div class="mail">
        <a href="mailto:gralypho@gmail.com "> <i class="fa-solid fa-envelope contact-icon "></i></a>
      </div>
      <div class="tel"><a href="tel:0672901614" ><i class="fa-solid fa-phone-volume contact-icon"></i></a></div>
    </div>
  </div>
</section>

<style>
  .H-section {
    display: flex;
    flex-direction: column;
    height: 100vh;
    font-size: 16px;
    opacity: 1;
    justify-content: center;
    align-items: center;
  }
    .wrapper-png {
    display: grid;
    grid-template-columns: repeat(4, 1fr);
    grid-template-rows: 1;
    margin-top: -100px;
  }
    .climb {
      grid-column: 6 / span 6;
      grid-row: 1;
    height: 160px;
    z-index: 2;
    margin-top: -80px;
    align-self: center;
  }
  .six {
    grid-column: 6 / span 6;
      grid-row: 1;
    height: 115px;
    z-index: 1;
    margin-top: 0px;
  }
  .wrapper-text {
    display: flex;
    flex-direction: column;
    border-radius: 20px;
    padding: 20px;
  }
  .H-section h1 {
    text-align: center;
    font-family: epilogue;
    font-weight: 600;
    font-size: var(--xl);
    color: white;
    margin-top: 50px;
    padding: 10px;
  }
  .H-section h1 span {
    font-weight: 900;
    color: transparent;
    -webkit-background-image: linear-gradient(to left, var(--ca), var(--blue));
    background-image: linear-gradient(to left, var(--ca), var(--blue));
    -webkit-background-clip: text;
    background-clip: text;
  }

  .wrapper-contact {
    display: flex;
    flex-direction: column;
    background-color: var(--bg);
    height: auto;
    align-items: center;
    justify-content: center;
    padding: 20px;
    border-radius: 8px;
    gap: 10px;
    
  }
  /* .wrapper-contact h5 {
    color: white;
    font-family: kanit;
    font-weight: 200;
  } */
  .wrapper-media-contact {

    display: flex;
    gap: 40px;
    border: 1px solid rgb(103, 103, 103);
    padding: 20px;
    border-radius: 8px;
  }
  .contact-icon {
    color: var(--orange);
    font-size: 2em;
  }
  .contact-icon:hover{
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
  .gsap5 {
    background-color: transparent;
  }

</style>



  <!-- <h2>
      Le web c'est avant tout une passion. <br />Le code informatique c'est avant tout le langage créatif par
      excellence. Celui qui permet de tout faire et dont la seule limite est notre propre connaissance. <br /> Créer un
      service digital est avant tout une vocation. Aider, apporter des solutions, permettre à chaque entreprise de
      grandir et de se développer. <br /> Écouter est avant tout une qualité, chercher à comprendre l'histoire de
      l'entrepreneur, de l'indépendant, de la société, du collectif (...). <br />
      Gralypho est une agence Digitale éthique et responsable. Les tarifs, les délais, les objectifs sont toujours au coeur
      même de nos priorités et nous apprécions plus que tout de travailler dans la plus constructive des collaborations,
      à travers un échange sincère et enrichissant.
    </h2> -->