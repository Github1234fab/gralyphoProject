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
    <h2>
      Augmentez votre visibilité, simplifiez vos opérations et offrez à vos clients une expérience exceptionnelle !
    </h2>
    <h1>Optez pour nos solutions digitales <span>100% </span>sur mesure.</h1>

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
  <!-- <div class="wrapper-tree">
      <img src={mediaTree} alt="arbre de logos de médias" class="media-tree" />
    </div> -->
</section>

<style>
  .A-section {
    display: grid;
    grid-template-columns: repeat(12, 1fr);
    grid-template-rows: auto;
    height: 100%;
    font-size: 16px;
    z-index: 1;
    background-color: var(--primary);
  }

  .wrapper-title {
    grid-column: 2/12;
    height: 100%;
    width: 100%;
    border-radius: 20px;
    z-index: 0;
    overflow: hidden;
    margin-top: 10px;
    z-index: 1;
  }
  .icon {
    padding: 20px;
    font-size: 2em;
    color: var(--ca);
    border-radius: 5px;
  }

  .A-section h1 {
    word-wrap: break-word;
    z-index: 1;
    text-align: left;
    font-family: epilogue;
    font-weight: 900;
    font-size: 3em;
    color: white;
    line-height: 56px;
    margin-left: 60px;
    margin-top: 20px;
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
    margin-top: 100px;
    z-index: 1;
    font-family: epilogue;
    font-weight: 100;
    word-wrap: break-word;
    text-align: left;
    line-height: 30px;
    font-size: 1.1em;
    color: var(--colorC);
    margin-left: 60px;
  }
  .wrapper-images {
    display: flex;
    justify-content: left;
    align-items: center;
    margin-left: 44px;
    width: 100%;
    margin-top: 30px;
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
    border:  2px solid #7f00fd;
    border-radius: 8px;
    color: white;
    text-decoration: none;
    font-family: epilogue;
    font-weight: 400;
    font-size: 1em;
    box-shadow: inset 2px 2px 5px var(--colorO);
    margin-left: 63px;
    margin-top: 50px;
    padding: 30px;
    transition: 0.4s ease-in-out;
    margin-bottom: 50px;
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
  /* .wrapper-tree {
    grid-column: 2/12;
    display: flex;
    justify-content: center;
    align-items: center;
    width: 100%;
    height: auto;
    margin-top: -150px;
    z-index: 0;
  }
  .media-tree {
    width: 400px;
    height: 300px;
    margin-left: 400px;
  } */

  @media screen and (max-width: 892px) {
    /* .media-tree {
      width: 300px;
      height: 200px;
      margin-left: 300px;
    } */

    /* .wrapper-tree {
      display: flex;
      justify-content: center;
      align-items: center;
      width: 100%;
      height: auto;
      margin-top: -120px;
    } */
  }

  @media screen and (max-width: 627px) {
    .wrapper-images {
      display: flex;
      justify-content: left;
      align-items: center;
      margin-left: 30px;
      gap: 23px;
      width: 100%;
      margin-top: 30px;
    }
    .icon {
      font-size: 1.6em;
    }
    .A-section {
      font-size: 14px;
    }
    .wrapper-title {
      overflow: hidden;
      height: auto;
    }
    /* .media-tree {
 visibility: hidden;
    } */
  }
</style>
