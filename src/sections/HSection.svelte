<script>
  import Climber from "../Assets/png-gralypho/Saly-15.png";
  import six from "../Assets/png-gralypho/six.svg";

  import { onMount } from "svelte";

  onMount(() => {
    gsap.to(".gsap5", {
      rotate: 370,
      scale: 1,
      scrollTrigger: {
        trigger: ".gsap5",
        start: "top 600px",
        end: "-300px",
        scrub: 2,
      },
    });
  });
</script>

<section class="H-section">
  <div class="wrapper-text">
    <img src={Climber} alt="" class="climb gsap5" />
    <img src={six} alt="" class="six gsap5" />
    <h1>L'agence <strong>Gralypho</strong>, l'expertise et l'expérience <span>100% </span>gagnante !</h1>
    <h2>Le web c'est avant tout une passion. <br>Le code informatique c'est avant tout le langage créatif par excellence. Celui qui permet de tout faire et dont la seule limite est notre propre connaissance. <br>  Créer un service digital est avant tout une vocation. Aider, apporter des solutions, permettre à chaque entreprise de grandir et de se développer. <br> Écouter est avant tout une qualité, chercher à comprendre l'histoire de l'entrepreneur, de l'indépendant, de la société, du collectif (...).  <br>
      Gralypho est une agence Digitale éthique et responsable. Les tarifs, les délais, les objectifs sont toujours au coeur même de nos priorités et nous apprécions plus que tout  de travailler dans la plus constructive des collaborations, à travers un échange sincère et enrichissant.</h2>
  </div>
</section>

<style>
  .H-section {
    display: grid;
    grid-template-columns: repeat(12, 1fr);
    grid-template-rows: auto;
    height: 100%;
    font-size: 16px;
    background-color: var(--colorO);
    margin-top: 150px;
  }
  .wrapper-text {
    grid-column: 2/12;
    grid-row: 2;
    display: flex;
    flex-direction: column;
    border-radius: 20px;
    padding: 20px;
    border: solid 1px rgb(55, 55, 55);
  }
  .H-section h1 {
    word-wrap: break-word;
    text-align: left;
    font-family: epilogue;
    font-weight: 500;
    font-size: 1.7em;
    color: white;
    margin-top: 50px;
    padding: 10px;
    line-height: 37px;
  }
  .H-section h1 span {
    font-weight: 600;
    color: transparent;
    background-clip: text;
    background-image: linear-gradient(to left, var(--colorD), var(--colorI));
  }
  .H-section h2 {
    word-wrap: break-word;
    margin-top: 10px;
    font-family: epilogue;
    font-weight: 300;
    font-size: 1.2em;
    color: var(--colorC);
    text-align: left;
    padding: 10px;
    line-height: 30px;
  }
  .gsap5 {
    background-color: transparent;
  }

  .climb {
    height: 160px;
    margin-top: 40px;
    z-index: 2;
    align-self: center;
  }

  .six {
    height: 160px;
    margin-top: -130px;
    z-index: 1;
    align-self: center;
  }

  @media screen and (max-width: 768px) {
    .H-section {
      font-size: 13px;
    }
  }
</style>
