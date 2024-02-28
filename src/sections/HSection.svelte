<script>

  import { onMount } from "svelte";
  import Header from "../sections/Header.svelte";
  import Engrenage from "../Components/Engrenages.svelte";


</script>

<Header />
<section class="H-section">
    <div class="wrapper-text">
      <h1><span>Imaginer, <br> Développer,<br>  Créer.</span></h1>
              <h2>
                <span>Gralypho</span> est une agence <span>WEB </span>qui aide les entreprises <br> à accéder à <span>plus de visibilité</span> et <span>plus de clients sur internet</span>, <br> grâce à des solutions digitales adaptées à leur <span>besoin.</span> 

      </h2>
    <div class="wrapper-contact">
      <a href="/#footer">Contactez-nous</a>
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
    height: 100vh;
    font-size: 16px;
    opacity: 1;
  }
  
  .wrapper-text {
    grid-column: 2 / span 12;
    grid-row: 1;
    display: flex;
    flex-direction: column;
    border-radius: 20px;
    align-items: baseline;
    margin-top: 20px;
  }
  .H-section h1 {
    text-align: left;
    font-family: epilogue;
    font-weight: 700;
    font-size: var(--xlhero);
    color: white;
    text-transform: capitalize;
    letter-spacing: -8px;
  }
  /* .H-section h1 span {
    font-weight: 900;
    color: transparent;
    -webkit-background-image: linear-gradient(to left, var(--orange), var(--blue));
    background-image: linear-gradient(to left, var(--orange), var(--blue));
    -webkit-background-clip: text;
    background-clip: text;
  } */
  .H-section h2 {
    font-family: poppins;
    font-weight: 300;
    font-size: var(--m);
    color: white;
    text-align: left;
    line-height: 40px;
    word-spacing: -2px;
  }
  .H-section h2 span {
    font-weight: 500;
    color: white;
  }

  .wrapper-contact {
    margin-top: 30px;
    display: flex;
    flex-direction: column;
    align-items: center;
    justify-content: center;
    background-color: var(--bg);
    height: auto;
    width: 200px;
    padding: 20px;
    text-align: center;
    border-radius: 4px;
    gap: 10px;
    background-color: var(--ca);
  }
  .wrapper-contact:hover {
    animation: bounce 0.4s ease-in-out;
  }

  .wrapper-contact a {
    text-decoration: none;
    color: var(--colorC);
    font-family: kanit;
    font-weight: 400;
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
  /* .gsap5 {
    background-color: transparent;
  } */
</style>
