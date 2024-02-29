<script>
  import { onMount } from "svelte";
  import Header from "../sections/Header.svelte";
  import Engrenage from "../Components/Engrenages.svelte";
</script>

<Header />
<section class="H-section">
  <div class="wrapper-text">
    <h1><span>Imaginer, <br /> Développer,<br /> Créer.</span></h1>
    <h2>
      <span>Gralypho</span> est une agence <span>WEB </span>qui aide les entreprises <br /> à accéder à
      <span>plus de visibilité</span>
      et <span>plus de clients sur internet</span>, <br /> grâce à des solutions digitales adaptées à leur
      <span>besoin.</span>
    </h2>
    <a class="contact" href="/#footer">Nous contacter</a>
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
    height: 100vh;
    font-size: 16px;
    opacity: 1;
  }

  .wrapper-text {
    grid-column: 1 / 8;
    grid-row: 1/3;
    display: flex;
    flex-direction: column;
    border-radius: 20px;
    margin-top: 40px;
    margin-left: 100px;
  }
  .H-section h1 {
    text-align: left;
    font-family: epilogue;
    font-weight: 700;
    font-size: var(--xlhero);
    color: white;
    text-transform: capitalize;
    letter-spacing: -8px;
    line-height: 135px;
  }

  .H-section h2 {
    font-family: poppins;
    font-weight: 300;
    font-size: var(--m);
    color: white;
    text-align: left;
    line-height: 40px;
    word-spacing: -2px;
    margin-top: 20px;
    margin-left: 10px;
  }
  .H-section h2 span {
    font-weight: 500;
    color: white;
  }
  .contact {
    text-decoration: none;
    color: var(--colorC);
    background-color: var(--ca);
    font-family: kanit;
    font-weight: 400;
    margin-top: 30px;
    margin-left: 0px;
    width: 200px;
    padding: 25px;
    border-radius: 6px;
    text-align: center;
  }
  .contact:hover {
    animation: bounce 0.4s ease-in-out;
  }

  .wrapper-visuel {
    grid-column: 8/12;
    grid-row: 1/3;
    display: flex;
    justify-content: center;
    align-items: center;
    gap: 0px;
    margin-top: 200px;
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
    .wrapper-text {
      margin-top: 100px;
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
      margin-top: 80px;
      z-index: 0;
    }
    .contact {
      margin-top: 50px;
      margin-left: 10px;
      padding: 10px;
      font-size: 1em;
    }
  }

  @media only screen and (min-width: 1100px) and (max-width: 1400px) {
    .wrapper-text {
      margin-top: 50px;
      z-index: 2;
      margin-left: 30px;
    }
    .H-section h1 {
      font-size: 8em;
      line-height: 120px;
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
      margin-top: 150px;
      margin-left: -20px;
      z-index: 0;
    }
    .contact {
      margin-top: 50px;
      margin-left: 10px;
      padding: 10px;
      font-size: 1em;
    }
  }
  @media only screen and (min-width: 768px) and (max-width: 1100px) {
    .wrapper-text {
      margin-top: 100px;
      z-index: 2;
      margin-left: 30px;
      grid-column: 1/9;
    }
    .H-section h1 {
      font-size: 6em;
      line-height: 100px;
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
      margin-top: 300px;
      margin-left: -20px;
      z-index: 0;
    }
    .contact {
      margin-top: 50px;
      margin-left: 10px;
      padding: 10px;
      font-size: 1em;
    }
  }
  @media only screen and (min-width: 576px) and (max-width: 768px) {
     .wrapper-text {
      margin-top: 10px;
      margin-bottom: 40px;
      z-index: 2;
      margin-left: 0px;
      grid-column: 1/13;
      background-color: rgba(4, 8, 33, 0.182);
      backdrop-filter: blur(8px);
      padding: 20px;
      border-radius: 0px;
    }
    .H-section h1 {
      font-size: 6em;
      line-height: 100px;
      letter-spacing: -5px;
    }
    .H-section h2 {
      margin-top: 40px;
    }
    .wrapper-visuel {
      grid-column: 1/13;
      grid-row: 1/3;
      display: flex;
      justify-content: center;
      align-items: center;
      gap: 0px;
      margin-top: 360px;
      margin-left: 40px;
      z-index: 0;
    }
    .contact {
      margin-top: 50px;
      margin-left: 10px;
      padding: 10px;
      font-size: 1em;
    }
  }
  @media only screen and (min-width: 300px) and (max-width: 576px) {
    .wrapper-text {
      margin-top: 10px;
      margin-bottom: 40px;
      z-index: 2;
      margin-left: 0px;
      grid-column: 1/13;
      background-color: rgba(4, 8, 33, 0.182);
      backdrop-filter: blur(8px);
      padding: 20px;
      border-radius: 0px;
    }
    .H-section h1 {
      font-size: 3.3em;
      line-height: 60px;
      letter-spacing: -3px;
    }
    .H-section h2 {
      margin-top: 40px;
         line-height: 25px;
    }
    .wrapper-visuel {
      grid-column: 1/13;
      grid-row: 1/3;
      display: flex;
      justify-content: center;
      align-items: center;
      gap: 0px;
      margin-top: 360px;
      margin-left: -45px;
      z-index: 0;
    }
    .contact {
      margin-top: 50px;
      margin-left: 10px;
      padding: 10px;
      font-size: 1em;
    }
  }
</style>
