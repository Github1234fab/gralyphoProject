<script>
</script>

<section class="difference">
  <h1>Pourquoi choisir <span>Gralypho?</span></h1>
  <p>
    <span>Gralypho</span> est une agence digitale, spécialisé dans la <span>conception de site Web</span> et dans la
    <span>création d'application </span>sur mesure. Notre expertise dans le domaine du Web est profonde et solide.
    <br /><br />
    Nous sommes formés aux métiers du Web. C'est à dire que nos <span>connaissances </span> en matières de design, de
    référencement, de normes d'accessibilité W3C, d'organisation de contenu textuel et visuel sont optimales. Cela
    signifie aussi que nous sommes <span>formés au code informatique</span> c'est à dire que nous avons les moyens de
    savoir exactement ce qu'un site contient, sous le capot. <br />
    Faire confiance à <span>l'agence Gralypho</span>, c'est faire le choix de la qualité, de la sécurité, de la
    performance et de la pérennité. <br /><br />Nous somme ici pour vous accompagner dans la <span>réalisation </span>de
    votre projet, de sa conception à sa mise en ligne. Nous sommes là pour vous conseiller, vous guider et vous former.
    Nous sommes là pour vous aider à atteindre vos
    <span>objectifs</span> et à les dépasser en vous proposant et en concevant des fonctionnalités, des outils, des solutions
    qui vous permettront de vous démarquer à coup sûr, de la concurrence.
  </p>
</section>

<style>
  .difference {
    display: flex;
    flex-direction: column;
    align-items: center;
    justify-content: center;
    height: auto;
    font-size: 16px;
    background-color: white;
    padding: 40px;
    margin: 0px auto;
    width: calc(100vw - 100px);
  }
  .difference h1 {
    font-family: epilogue;
    font-size: var(-l);
    color: #2d2d2d;
    font-weight: 900;
    margin-bottom: 40px;
    letter-spacing: -0.04em;
    margin-top: 20px;
  }
  .difference h1 span {
    color: transparent;
        -webkit-background-image: linear-gradient(to left, #ff8a00, var(--blue2));
    background-image: linear-gradient(to left, #ff8a00, var(--blue2));
    -webkit-background-clip: text;
    background-clip: text;
        font-weight: 900;
  }
  .difference p {
    margin-top: 40px;
    font-family: poppins;
    color: grey;
    column-count: 2;
    font-size: var--(m);
    color: #2d2d2d;
    font-weight: 400;
    line-height: 1.5em;
    width: 100%;
  }
  .difference p span {
    font-family: epilogue;
    color: grey;
    font-size: var--(m);
    color: orange;
    font-weight: 700;
    line-height: 1.5em;
    width: 100%;
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

  @media screen and (max-width: 768px) {
    .difference {
      width: calc(100vw - 10px);
    }
    .difference p {
      column-count: 1;
    }
  }
</style>
