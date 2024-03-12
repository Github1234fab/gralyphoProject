<script>
  import { onMount } from "svelte";
  import Header from "../sections/Header.svelte";
  import Engrenage from "../Components/Engrenages.svelte";
  import { fade } from "svelte/transition";

  let textIndex = 0;
  let textTab = [" de Site Internet", "d'Application Web"];

  onMount(() => {
    setInterval(() => {
      textIndex = (textIndex + 1) % textTab.length;
    }, 1200);
  });
</script>

<Header />
<section class="H-section">
  <div class="wrapper-text">
    <h1>Imaginer, <br /> Développer,<br /> Créer. <br /></h1>
    <h3>Conception <span>{textTab[textIndex]}</span> </h3>
    <h2>
      Nous créeons des sites Web et des Applications sur mesure pour tous les professionnels souhaitant obtenir des
      résultats tangibles à propos du <span> gain de productivité et de temps</span>, et de
      <span>la conversion de clients</span>.<br />
    </h2>
    <div class="wrapper-contact">
      <a class="contact" href="/#footer">Nous contacter</a>
      <a class="contact2" href="/#footer">Devis gratuit</a>
    </div>
  </div>

  <div class="wrapper-visuel">
    <Engrenage />
  </div>
</section>

<style>
  .H-section {
    display: grid;
    grid-template-columns: repeat(12, 1fr);
    grid-template-rows: auto;
    height: 900px;
    font-size: 16px;
    opacity: 1;
    background-color: white;
    margin-bottom: 200px;
  }
  .wrapper-text {
    grid-column: 1 / 8;
    grid-row: 1/3;
    display: flex;
    flex-direction: column;
    border-radius: 20px;
    margin-left: 100px;
  }
  .H-section h1 {
    text-align: left;
    font-family: epilogue;
    font-weight: 900;
    font-size: var(--xlhero);
    color: var(--primary);
    text-transform: capitalize;
    letter-spacing: -8px;
    line-height: 135px;
    margin-top: 70px;
  }
  .H-section h3 {
    font-family: poppins;
    font-weight: 500;
    font-size: var(--l);
    letter-spacing: -2px;
    color: grey;
    transition: 1s ease-in-out;
    margin-left: 5px;
  }
    .H-section h3 span {
color: var(--colorI);
  }
  .H-section h2 {
    font-family: poppins;
    font-weight: 300;
    font-size: var(--m);
    color: grey;
    text-align: left;
    line-height: 30px;
    margin-top: 20px;
    margin-left: 10px;
  }
  .H-section h2 span {      
    font-weight: 600;
    color: rgb(84, 84, 84);
  }
  .contact {
    text-decoration: none;
    color: white;
    background-color: var(--CTA);
    font-family: kanit;
    font-weight: 400;
    margin-top: 0px;
    margin-left: 0px;
    width: 160px;
    border-radius: 6px;
    text-align: center;
    padding: 20px;
    box-shadow: 0px 0px 10px 2px rgba(76, 76, 76, 0.35);
  }
  .contact2 {
    text-decoration: none;
    color: white;
    background-color: var(--CTA2);
    font-family: kanit;
    font-weight: 400;
    margin-top: 10px;
    margin-left: 10px;
    width: 160px;
    border-radius: 6px;
    text-align: center;
    padding: 20px;
    box-shadow: 0px 0px 10px 2px rgba(76, 76, 76, 0.35);
  }
  .contact:hover {
    animation: bounce 0.4s ease-in-out;
  }
  .contact2:hover {
    animation: bounce 0.4s ease-in-out;
  }
  .wrapper-contact {
    display: flex;
    flex-direction: column;
    gap: 0px;
    margin-top: 20px;
    align-items: baseline;
    justify-content: flex-start;
  }

  .wrapper-visuel {
    grid-column: 8/12;
    grid-row: 1/3;
    display: flex;
    /* justify-content: center;
    align-items: center; */
    gap: 0px;
    margin-top: 530px;
    margin-left: 0px;
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

  @media only screen and (min-width: 1400px) and (max-width: 1900px) {
    .H-section {
      height: 900px;
    }
    .wrapper-text {
      margin-top: 0px;
      z-index: 2;
    }
    .H-section h1 {
      font-size: 9em;
      line-height: 120px;
      letter-spacing: -7px;
    }
    .H-section h2 {
      margin-top: 20px;
    }
    .wrapper-visuel {
      grid-column: 8/11;
      grid-row: 1/3;
      display: flex;
      justify-content: center;
      align-items: center;
      gap: 0px;
      margin-top: 530px;
      margin-left: 0px;
      z-index: 0;
    }
    .contact {
      margin-top: 50px;
      margin-left: 10px;

      font-size: 1em;
    }
  }

  @media only screen and (min-width: 1100px) and (max-width: 1400px) {
    .wrapper-text {
      margin-top: 0px;
      z-index: 2;
      margin-left: 30px;
    }
    .H-section h1 {
      font-size: 8em;
      line-height: 113px;
      letter-spacing: -7px;
    }
    .H-section h2 {
      margin-top: 40px;
    }
    .wrapper-visuel {
      grid-column: 8/12;
      grid-row: 1/3;
      display: flex;
      justify-content: center;
      align-items: center;
      gap: 0px;
      margin-top: 530px;
      margin-left: 0px;
      z-index: 0;
    }
    .contact {
      margin-top: 50px;
      margin-left: 10px;

      font-size: 1em;
    }
  }
  @media only screen and (min-width: 768px) and (max-width: 1100px) {
    .wrapper-text {
      margin-top: 0px;
      z-index: 2;
      margin-left: 30px;
      grid-column: 1/9;
    }
    .H-section h1 {
      font-size: 6em;
      line-height: 0.9em;
      letter-spacing: -5px;
    }
    .H-section h2 {
      margin-top: 40px;
    }
    .wrapper-visuel {
      grid-column: 9/12;
      grid-row: 1/3;
      display: flex;
      justify-content: center;
      align-items: center;
      gap: 0px;
      margin-top: 630px;
      margin-left: -230px;
      z-index: 0;
    }
    .contact {
      margin-top: 50px;
      margin-left: 10px;
      font-size: 1em;
    }
  }
  @media only screen and (min-width: 576px) and (max-width: 768px) {
    .wrapper-text {
      margin-top: -50px;
      margin-bottom: 40px;
      z-index: 2;
      margin-left: 5px;
      grid-column: 1/13;
      padding: 20px;
      border-radius: 0px;
    }
    .H-section h1 {
      font-size: 6em;
      line-height: 0.9em;
      letter-spacing: -5px;
    }
    .H-section h2 {
      margin-top: 40px;
    }
    .wrapper-visuel {
      grid-column: 1/13;
      grid-row: 2/3;
      display: flex;
      justify-content: center;
      align-items: center;
      gap: 0px;
      margin-top: -260px;
      margin-left: 240px;
      z-index: 0;
    }
    .contact {
      margin-top: 50px;
      margin-left: 10px;
      font-size: 1em;
    }
  }
  @media only screen and (min-width: 300px) and (max-width: 576px) {
    .H-section {
      height: 720px;
    }
    .wrapper-text {
      margin-top: -50px;
      margin-bottom: 40px;
      z-index: 2;
      margin-left: 0px;
      grid-column: 1/13;
      padding: 20px;
      border-radius: 0px;
    }
    .H-section h1 {
      font-size: 3.1em;
      line-height: 0.9em;
      letter-spacing: -0.05em;
    }
    .H-section h3 {
      margin-top: 10px;
      font-size: 1.4em;
      line-height: 0.9em;
      letter-spacing: -0.04em;
    }
    .H-section h2 {
      margin-top: 30px;
      line-height: 25px;
      font-size: 1em;
    }

    .wrapper-visuel {
      grid-column: 5/13;
      grid-row: 1;
      display: flex;
      justify-content: center;
      align-items: center;
      gap: 0px;
      margin-top: 530px;
      margin-left: 27px;
      z-index: 0;
    }
    .contact {
      margin-top: 30px;
      margin-left: 10px;
      font-size: 1em;
    }
    .contact2 {
      margin-top: 10px;
      margin-left: 10px;
      font-size: 1em;
    }
  }
</style>
