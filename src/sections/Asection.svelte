<script>
  import background from "../Assets/png-gralypho/17.png";
    import background2 from "../Assets/png-gralypho/41.png";
      import background3 from "../Assets/png-gralypho/09.png";
       import background4 from "../Assets/png-gralypho/21.png";
        import background5 from "../Assets/png-gralypho/30.png";
</script>

<section class="A-section" >
  <div class="wrapper-title">
    <h1>Optez pour nos solutions digitales <span>100% </span>sur mesure.</h1>
    <h2>
      Augmentez votre visibilité, simplifiez vos opérations et offrez à vos clients une expérience exceptionnelle !
    </h2>
    <a class="link" href="/#sectionE">Découvrir</a>
    <div class="wrapper-images">
    <!-- <img src={background2} alt="" class="background" /> -->
        <!-- <img src={background} alt="" class="background" />
            <img src={background3} alt="" class="background" /> -->
            <!-- <img src={background4} alt="" class="background" />
            <img src={background5} alt="" class="background" /> -->
    </div>
  </div>
</section>

<style>
  .A-section {
    display: grid;
    grid-template-columns: repeat(12, 1fr);
    grid-template-rows: auto;
    height: auto;
    font-size: 16px;
    margin-bottom: 50px;
  }

  .wrapper-title {
    grid-column: 2/12;
    height: 90%;
    width: 100%;
    border-radius: 20px;
    margin-top: 20px;
    z-index: 0;
    overflow: hidden;
  
  }

  .A-section h1 {
    word-wrap: break-word;
    z-index: 1;
    text-align: left;
    font-family: epilogue;
    font-weight: 500;
    font-size: 1.8em;
    color: white;
    line-height: 37px;
    padding: 30px;
    margin-top: 10px;
  }
  .A-section h1 span {
    font-weight: 600;
    color: transparent;
    -webkit-background-image:inear-gradient(to left, var(--colorD), var(--colorI));
    background-image: linear-gradient(to left, var(--colorD), var(--colorI));
    -webkit-background-clip: text;
    background-clip: text;
  }
  .A-section h2 {
    margin-top: -50px;
    z-index: 1;
    font-family: epilogue;
    font-weight: 300;
    word-wrap: break-word;
    text-align: left;
    line-height: 30px;
    font-size: 1.1em;
    color: var(--colorC);
    padding: 30px;
  }
  .wrapper-images{
width:100%;
    display: flex;
    align-items: center;
    justify-content: center;
    gap: 30px;
    margin-top: 60px;
    overflow: hidden;
    border-radius: 40px 40px 30px 60px;

  }
  .background {
    padding: 40px;
    width:auto;
    height: 600px;
    box-shadow: 6px 10px 15px black;

    /* z-index: 0; */
  }

  .link {
    display: flex;
    z-index: 2;
    justify-content: center;
    align-items: center;
    width: 150px;
    height: 3.1em;
    background: linear-gradient(to left, var(--colorJ), var(--colorI));
    border: none;
    border-radius: 8px;
    color: white;
    text-decoration: none;
    font-family: epilogue;
    font-weight: 400;
    font-size: 1em;
    box-shadow: inset 2px 2px 5px var(--colorO);
    margin-left: 30px;
    margin-top: 20px;
    margin-bottom: 30px;
    padding: 30px;
    transition: 0.4s ease-in-out;
  }
  .link:hover {
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

   @media screen and (max-width: 590px) {
    .A-section {
      font-size: 15px;
    }
    .wrapper-title {
      overflow: hidden;
      height: auto;
    }
    .background {
      width: auto;
      height: 420px;
      z-index: 0;
      margin-top: 30px;
      margin-left: -50px;
      margin-bottom: 0px;
    }
  } 
    @media screen and (max-width: 491px) {
    .background {
      margin-left: -130px;
    }
  } 
</style>
