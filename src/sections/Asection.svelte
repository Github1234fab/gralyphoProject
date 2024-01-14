<script>
  // import background from "../Assets/png-gralypho/Saly-43.png";
  // import background2 from "../Assets/png-gralypho/Saly-44.png";
  import background3 from "../Assets/png-gralypho/09.png";
  import background4 from "../Assets/png-gralypho/21.png";
  import background5 from "../Assets/png-gralypho/30.png";
  import dev from "../Assets/png-gralypho/Saly-15.png";
  import world from "../Assets/png-gralypho/Saly-44.png";
  import mediaTree from "../Assets/png-gralypho/applis.png";
  import Header from "../sections/Header.svelte";
</script>

<section class="A-section">
  <Header />
  <div class="wrapper-title">
    <!-- <h1>Optez pour nos solutions digitales <span>100% </span>sur mesure.</h1> -->
    <h1>Chez <span>Gralypho</span>, nous transformons l'ordinaire en extraordinaire !</h1>
    <h2>
      Augmentez votre visibilité, simplifiez vos opérations et offrez à vos clients une expérience exceptionnelle !
    </h2>
    <!-- avec  <span>Gralypho</span>, votre partenaire Digital -->

    <!-- <div class="wrapper-images">
      <i class="fa-solid fa-desktop banner-icon icon"></i>
      <i class="fa-solid fa-sitemap icon"></i>
      <i class="fa-solid fa-magnifying-glass-chart banner-icon icon"></i>
      <i class="fa-solid fa-comments-dollar banner-icon icon"></i>
      <i class="fa-solid fa-recycle icon"></i>
      <i class="fa-solid fa-wand-magic-sparkles banner-icon icon"></i>
    </div> -->
    <a class="link" href="/#sectionE">Découvrir</a>
  </div>
  <!-- <div class="wrapper-tree">
      <img src={mediaTree} alt="arbre de logos de médias" class="media-tree" />
    </div> -->
</section>

<style>
  .A-section {
    display: grid;
    grid-template-columns: repeat(12, 1fr);
    grid-template-rows: auto;
    height: auto;
    font-size: 16px;
    z-index: 1;
    background-color: var(--primary);
  }
  .wrapper-title {
    grid-column: 1/12;
    height: 100%;
    width: 100%;
    border-radius: 20px;
    z-index: 0;
    overflow: hidden;
    margin-top: 30px;
    z-index: 1;
  }
  /* .icon {
    padding: 20px;
    font-size: 2em;
    color: var(--ca);
    border-radius: 5px;
  } */
  .A-section h1 {
    z-index: 1;
    text-align: left;
    font-family: epilogue;
    font-weight: 900;
    font-size: 3em;
    color: white;
    line-height: 56px;
    margin-left: 50px;
    margin-top: 40px;
  }
  .A-section h1 span {
    font-weight: 800;
    color: transparent;
    -webkit-background-image: inear-gradient(to left, var(--ca), var(--blue));
    background-image: linear-gradient(to left, var(--ca), var(--blue));
    -webkit-background-clip: text;
    background-clip: text;
  }
  .A-section h2 {
    z-index: 1;
    font-family: epilogue;
    font-weight: 100;
    word-wrap: break-word;
    text-align: left;
    line-height: 20px;
    font-size: 1.1em;
    color: var(--colorC);
    margin-left: 50px;
    margin-top: 20px;
  }

  .link {
    display: flex;
    z-index: 3;
    justify-content: center;
    align-items: center;
    width: 150px;
    height: 3.1em;
    /* background-color: #7f00fd; */
    /* background: linear-gradient(to left, var(--colorJ), var(--colorI)); */
    border: 2px solid #7f00fd;
    border-radius: 8px;
    color: white;
    text-decoration: none;
    font-family: epilogue;
    font-weight: 400;
    font-size: 1em;
    box-shadow: inset 2px 2px 5px var(--colorO);
    margin-left: 50px;
    margin-top: 100px;
    padding: 30px;
    transition: 0.4s ease-in-out;
    margin-bottom: 100px;
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

  @media screen and (max-width: 768px) {
    .wrapper-title {
      overflow: hidden;
      height: auto;
    }
    .A-section {
      font-size: 12px;
    }
  }
</style>
