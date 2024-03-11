<script>
  import Dev from "../Assets/png-gralypho/dev.png";
  import Carousel from "../Components/CarousselCards.svelte";
  import skate from "../Assets/png-gralypho/skateboard.png";
  import { onMount } from "svelte";
  import { bounceIn } from "svelte/easing";
  import Ville from "../Assets/png-gralypho/05.png";
    import Visuel from "../Assets/png-gralypho/05.png";
        import VisuelB from "../Assets/png-gralypho/21.png";
            import VisuelC from "../Assets/png-gralypho/36.png";

  // onMount(() => {
  //   // function handleResize() {
  //     if (window.innerWidth < 576) {
  //       gsap.to(".wrapper-developpeur", {
  //         x: 200,
  //         // ease: power4,
  //         scrollTrigger: {
  //           trigger: ".wrapper-developpeur",
  //           start: "top 920px",
  //           end: "-100px",
  //           scrub: 5,
  //         },
  //       });
  //     }
  //     else if (window.innerWidth < 768) {
  //       gsap.to(".wrapper-developpeur", {
  //         x: 400,
  //         // ease: power4,
  //         scrollTrigger: {
  //           trigger: ".wrapper-developpeur",
  //           start: "top 920px",
  //           end: "-100px",
  //           scrub: 5,
  //         },
  //       });
  //     } else {
  //       gsap.to(".wrapper-developpeur", {
  //         x: 700,
  //         // ease: power4,
  //         scrollTrigger: {
  //           trigger: ".wrapper-developpeur",
  //           start: "top 920px",
  //           end: "-100px",
  //           scrub: 5,
  //         },
  //       });
  //     }
  //   });

    // // Appeler la fonction de gestion de redimensionnement au chargement initial
    // handleResize();

    // // Ajouter un écouteur d'événement pour le redimensionnement de la fenêtre
    // window.addEventListener("resize", handleResize);

    // // Nettoyer l'écouteur d'événement lors de la destruction du composant
    // return () => {
    //   window.removeEventListener("resize", handleResize);
    // };
  
</script>

<section class="G-section">
    <div class="wrapper-title-img">
      <div class="wrapper-visuels">
     <!-- <img src={Ville} alt="png d'une illustration d'environnement média Web" class="ville" /> -->
          <!-- <img src={VisuelB} alt="png d'une illustration d'environnement média Web" class="ville" /> -->
          </div>
      <div class="wrapper-text">
        <h1>Découvrez nos <span>réalisations </span></h1>
         <h2>
      Découvrez ici des projets témoins utilisant chacun une technique particulière. Découvrez vite le potentiel des
      animations, des applications, des requêtes API, des jeux, des composants. (...) !
    </h2>
    </div> 
          <div class="wrapper-visuels">
         <img src={Visuel} alt="png d'une illustration d'environnement média Web" class="ville" />
              <!-- <img src={VisuelC} alt="png d'une illustration d'environnement média Web" class="ville" /> -->
              </div>
     </div>
  <Carousel />
</section>

<style>
  .G-section {
    display: grid;
    grid-template-columns: repeat(12, 1fr);
    grid-template-rows: auto;
    height: auto;
    width: 100%;
    font-size: 16px;
    background-color: rgb(250, 250, 250);
  }
    .wrapper-title-img {
   grid-column: 1/12;
  display: flex;
  justify-content: flex-start;
  align-items: flex-start;  
  margin: 80px auto;
  gap: 30px;
  }
  .wrapper-text {
    display: flex;
    flex-direction: column;
    align-items: center;
    justify-content:center;
    gap: 30px;
  }
  .wrapper-visuels {
    display: flex;
    flex-direction: column;
    align-items: center;
    justify-content: center;
  }

  .G-section h1 {
    text-align: center;
    font-family: epilogue;
    font-weight: 900;
    font-size: var(--xl);
    color: var(--primary);
    letter-spacing: -1px;
    line-height: 1em;
  }
  .G-section h1 span {
    font-weight: 900;
    color: transparent;
    -webkit-background-image: linear-gradient(to left, var(--ca), var(--blue));
    background-image: linear-gradient(to left, var(--ca), var(--blue));
    -webkit-background-clip: text;
    background-clip: text;
  }

  .G-section h2 {
    font-family: poppins;
    font-weight: 300;
    font-size: var(--m);
    color: grey;
    text-align: left;
    line-height: 25px;
    letter-spacing: -1px;
    width: 70%;
    text-align: center;
  }

  .ville {
    width: auto;
    height: 250px;
    /* margin: 0 auto; */
    /* margin-top: 0px; */
    z-index: 0;
    border-radius: 20px;
  }


  @media screen and (max-width: 768px) {
  .G-section h1 {
    text-align: left;
    font-family: epilogue;
    font-weight: 900;
    font-size: var(--xl);
    color: var(--primary);
    letter-spacing: -1px;
    line-height: 40px;
  }
}
</style>
