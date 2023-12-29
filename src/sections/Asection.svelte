<script>
</script>

<section class="A-section">
  <div class="bar"></div>
  <div class="wrapper-title">
    <!-- <h1>Sites internet et applications sur mesures. <br> Boostez votre présence en ligne grâce aux outils digitaux.</h1> -->
    <h1>
      Nous aidons les entreprises à décoller vers le succès grâce à nos conceptions de Sites Web, 100% sur mesure.
    </h1>
    <!-- <h2> Offrez une solution d'exception à votre activité, grâce  à notre expertise en développement web</h2> -->
    <h2>
      Simplifiez vos opérations, augmentez votre visibilité et offrez à vos clients, une expérience exceptionnelle ! 
    </h2>
    <a class="link" href="/#sectionE">Découvrir</a>
  </div>
</section>

<style>
  .bar {
    width: 3000%;
    height: 2px;
    background-color: blue;
    box-shadow: 0px 5px 10px blue;
  }
  /* 41, 30, 23, 09"  */
  .A-section {
    display: grid;
    grid-template-columns: repeat(12, 1fr);
    grid-template-rows: auto;
    height: 700px;
    font-size: 16px;
    background-image: url(../Assets/png-gralypho/23.png);
    background-size: cover;
    background-position: center;
  }

  .wrapper-title {
    grid-column: 2/12;
    background-color: rgba(5, 5, 42, 0.687);
    height: 400px;
    width: 100%;
    border-radius: 20px;
    margin-top: 100px;
  }

  .A-section h1 {
    word-wrap: break-word;
    z-index: 4;
    text-align: left;
    font-family: epilogue;
    font-weight: 500;
    font-size: 1.8em;
    color: white;
    line-height: 35px;
    padding: 30px;
    margin-top: 30px;
  }

  .A-section h2 {
    margin-top: 0px;
    z-index: 2;
    position: relative;
    font-family: epilogue;
    font-weight: 300;
    word-wrap: break-word;
    text-align: left;
    font-size: 1em;
    color: var(--colorC);
    padding: 30px;
  }

  .link {
    display: flex;
    z-index: 2;
    justify-content: center;
    align-items: center;
    width: 30%;
    height: 3em;
    background-color: var(--colorJ);
    border: none;
    border-radius: 40px;
    color: white;
    text-decoration: none;
    font-family: epilogue;
    font-weight: 400;
    font-size: 1em;
    box-shadow:  2px 2px 5px var(--colorO);
    margin-left: 30px;
  }

  @media screen and (max-width: 768px){
    .A-section{
      font-size: 13px;
     
    }
    .wrapper-title{
       height: 410px;
    }
     .A-section h2 {
 line-height: 25px;
 margin-top: -40px;
  }
  }

    @media screen and (max-width: 590px){
    .A-section{
      font-size: 11px;
     
    }
    .wrapper-title{
       height: 450px;
    }
     .A-section h2 {
 line-height: 25px;
 margin-top: -40px;
  }
  }
</style>
