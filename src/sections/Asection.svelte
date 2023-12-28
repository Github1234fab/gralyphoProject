<script>
  import ordi from "../Assets/png-gralypho/Other 03.png";
  import port from "../Assets/png-gralypho/Other 17.png";
</script>

<section class="A-section">
  <div class="wrapper-title">
    <!-- <h1>Sites internet et applications sur mesures. <br> Boostez votre présence en ligne grâce aux outils digitaux.</h1> -->
    <h1>Sites internet et applications sur mesure conçus spécifiquement pour répondre à vos besoins.</h1>
    <!-- <h2> Offrez une solution d'exception à votre activité, grâce  à notre expertise en développement web</h2> -->
    <h2>
      Boostez votre présence en ligne avec nos solutions digitales exclusives, taillées sur mesure pour votre succès.
    </h2>
  </div>

  <a class="link" href="/#sectionE">Découvrir</a>
</section>

<style>
  /* 41, 30, 23, 09"  */
  .A-section {
    display: grid;
    grid-template-columns: repeat(12, 1fr);
    grid-template-rows: auto;
    height: 700px;
    margin-top: 0px;
    font-size: 16px;
    background-image: url(../Assets/png-gralypho/23.png);
    background-size: cover;
    background-repeat: no-repeat;
  }
  .wrapper-title {
    display: flex;
    flex-direction: column;
    grid-column: 2/12;
  }
  .wrapper-title::before {
    position: absolute;
    content: "";
    background-color: #11232e95;
    z-index: 0;
    height: 34%;
    width: 90%;
    margin-top: 50px;
    margin-left: -20px;
    padding: 30px;
    border-radius: 10px;
  }

  .A-section h1 {
    word-wrap: break-word;
    grid-column: 2/10;
    grid-row: 1;
    margin-top: 70px;
    font-family: epilogue;
    font-weight: bolder;
    font-size: 1.8em;
    color: white;
    position: relative;
    z-index: 1;
    /* text-transform: uppercase; */
  }

  .A-section h2 {
    word-wrap: break-word;
    grid-column: 2/10;
    grid-row: 1;
    font-family: epilogue;
    font-weight: 400;
    font-size: 1em;
    color: var(--colorC);
    margin-top: 20px;
    z-index: 2;
  }

  .link {
    grid-column: 2/12;
    grid-row: 2;
    display: flex;
    justify-content: center;
    align-items: center;
    width: auto;
    height: 3.3em;
    background-color: var(--colorA);
    border: none;
    border-radius: 40px;
    color: white;
    text-decoration: none;
    font-family: epilogue;
    font-weight: 400;
    font-size: 1em;
    margin-top: 260px;
    margin-bottom: 30px;
    box-shadow: inset 2px 2px 5px var(--colorO);
  }

  @media screen and (max-width: 760px) {
    .A-section {
      font-size: 13px;
      background-size: cover;
      background-repeat: no-repeat;
      height: 600px;
    }
    .wrapper-title::before {
      height: 35%;
    }
  }

  @media screen and (max-width: 620px) {
    .A-section {
      font-size: 12px;
      background-size: cover;
      background-position: center;
    }
    .A-section h2 {
      font-size: 1.1em;
    }
    .wrapper-title {
      margin-top: -20px;
    }
    .wrapper-title::before {
      height: 35%;
    }
  }

  @media screen and (max-width: 420px) {
    .A-section {
      font-size: 14px;
      height: 100%;
    }
    .A-section h1 {
      line-height: 27px;
      font-weight: 600;
    }
    .A-section h2 {
      font-size: 1.1em;
    }
    .wrapper-title {
      margin-top: 0px;
    }
    .wrapper-title::before {
      height: 50%;
    }
    .link {
      margin-top: 100px;
    }
  }
</style>
