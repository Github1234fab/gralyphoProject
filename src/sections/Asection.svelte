<script>
  // import background from "../Assets/png-gralypho/Saly-43.png";
  // import background2 from "../Assets/png-gralypho/Saly-44.png";
  import background3 from "../Assets/png-gralypho/09.png";
  import background4 from "../Assets/png-gralypho/21.png";
  import background5 from "../Assets/png-gralypho/30.png";

</script>

<section class="A-section">
  <div class="halo"></div>
  <div class="halo2"></div>
  <div class="wrapper-title">
    <h1>Optez pour nos solutions digitales <span>100% </span>sur mesure.</h1>
    <h2>
      Augmentez votre visibilité, simplifiez vos opérations et offrez à vos clients une expérience exceptionnelle !
    </h2>
    <div class="wrapper-images">
      <i class="fa-solid fa-desktop banner-icon icon"></i>
      <i class="fa-solid fa-sitemap icon"></i>
      <i class="fa-solid fa-magnifying-glass-chart banner-icon icon"></i>
      <i class="fa-solid fa-comments-dollar banner-icon icon"></i>
      <i class="fa-solid fa-recycle icon"></i>
      <i class="fa-solid fa-wand-magic-sparkles banner-icon icon"></i>
    </div>
    <a class="link" href="/#sectionE">Découvrir</a>
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
    margin-top: 50px;
    z-index: 1;
    background: radial-gradient(circle at top, var(--colorN), var(--colorO));
    background-size: 100% 100%;
    shape-outside: circle(90%);
    margin-left: 30px;
    margin-right: 30px;
    border-radius: 6px;
  }
  .A-section::after {
    content: "";
    position: absolute;
    top: 50px;
    left: 0;
    width: 100px;
    height: 100px;
    border-radius: 50%;
    background-color: beige;
    z-index: -1;
    opacity: 0.2;
  }

  .wrapper-title {
    grid-column: 2/12;
    height: 100%;
    width: 100%;
    border-radius: 20px;
    margin-top: 20px;
    z-index: 0;
    overflow: hidden;
  }
  .icon {
    color: var(--colorD);
    font-size: 2em;
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
    -webkit-background-image: inear-gradient(to left, var(--colorD), var(--colorI));
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
  .wrapper-images {
    display: flex;
    justify-content: left;
    align-items: center;
    margin-left: 30px;
    gap: 30px;
    width: 100%;
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
    margin-top: 50px;
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
    .icon {
      font-size: 1.2em;
    }
    .A-section {
      font-size: 15px;
    }
    .wrapper-title {
      overflow: hidden;
      height: auto;
    }
    /* .background {
      width: auto;
      height: 420px;
      z-index: 0;
      margin-top: 30px;
      margin-left: -50px;
      margin-bottom: 0px;
    } */
  }
</style>
