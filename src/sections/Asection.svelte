<script>
  import background from "../Assets/png-gralypho/17.png";
</script>

<section class="A-section" >
  <div class="wrapper-title">
    <h1>Optez pour nos solutions digitales <span>100% </span>sur mesure.</h1>
    <h2>
      Augmentez votre visibilité, simplifiez vos opérations et offrez à vos clients une expérience exceptionnelle !
    </h2>
    <a class="link" href="/#sectionE">Découvrir</a>
    <img src={background} alt="" class="background" />
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
    /* border: solid 1px rgb(55, 55, 55); */
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
    margin-top: -30px;
    z-index: 1;
    position: relative;
    font-family: epilogue;
    font-weight: 300;
    word-wrap: break-word;
    text-align: left;
    line-height: 30px;
    font-size: 1.1em;
    color: var(--colorC);
    padding: 30px;
  }
  .background {
    width: 100%;
    height: auto;
    z-index: 0;
    margin-top: 30px;
    margin-bottom: 50px;
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
