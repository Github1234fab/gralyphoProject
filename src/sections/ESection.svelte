<script>
  import SpaceShip from "../Assets/png-gralypho/Saly-43.png";
  import Banner from "../Components/Banner.svelte";

  import square from "../Assets/png-gralypho/square.svg";

  import { onMount } from "svelte";

  onMount(() => {
    gsap.to(".gsap2", {
      scale: 1.1,
      ease: "expoScale",
      scrollTrigger: {
        trigger: ".gsap2",
        start: "top 700px",
        end: "-200px",
        scrub: 1,
      },
    });
        gsap.to(".E-section", {
opacity: 1,
      ease: "E-section",
      scrollTrigger: {
        trigger: ".gsap2",
        start: "top 400px",
        end: "-200px",
        scrub: 1,
      },
    });
  });
</script>

<section class="E-section" id="sectionE">
  <div class="wrapper-text">
    <img src={SpaceShip} alt="" class="space-ship gsap2" />
    <img src={square} alt="" class="square gsap2" />
    <h1>Nos solutions digitales.</h1>
    <h2>
      Vous avez besoin d'un site vitrine, d'une application android? Ou alors, votre site internet date un peu et sans
      débourser une fortune, le relooker serait plutôt sympa ?! <br />Profitez de nos conseils en stratégie, de nos
      systèmes de composants intégrés et de notre expertise en référencement.
    </h2>
    <Banner />
  </div>
</section>

<style>
  .E-section {
    scroll-margin-top: 150px;
    display: grid;
    grid-template-columns: repeat(12, 1fr);
    grid-template-rows: auto;
    margin-top: 150px;
    margin-bottom: 50px;
    height: auto;
    font-size: 16px;
    background: radial-gradient(circle at top, var(--colorN), var(--colorO));
    background-size: 100% 100%;
    shape-outside: circle(90%);
    opacity: 0.2;
        margin-left: 30px;
    margin-right: 30px;
    border-radius: 6px;
  }
  .wrapper-text {
    grid-column: 2/12;
    grid-row: 2;
    display: flex;
    flex-direction: column;
    border-radius: 20px;
    padding: 20px;
    /* border: solid 1px rgb(55, 55, 55); */
    /* background-image: url(../Assets/png-gralypho/ggglitch.svg); */
    /* background-repeat: no-repeat;
    background-position: top;
    background-size: 27%; */
  }

  .E-section h1 {
    word-wrap: break-word;
    grid-column: 2/12;
    text-align: left;
    grid-row: 2;
    font-family: epilogue;
    font-weight: 800;
    font-size: 1.7em;
    color: white;
    margin-top: 50px;
    padding: 10px;
    line-height: 37px;
  }
  .E-section h2 {
    word-wrap: break-word;
    grid-column: 2/12;
    grid-row: 3;
    margin-top: 10px;
    font-family: epilogue;
    font-weight: 300;
    font-size: 1.2em;
    color: var(--colorC);
    text-align: left;
    padding: 10px;
    line-height: 30px;
  }
  .space-ship {
    height: 170px;
    transform: scale(0.7) rotate(50deg);
    z-index: 2;
    align-self: center;
    margin-top: 50px;
  }
  .square {
    height: 150px;
    transform: scale(0.7) rotate(0deg);
    z-index: 1;
    align-self: center;
    margin-top: -150px;
  }

  .gsap2 {
    background-color: transparent;
  }

  @media screen and (max-width: 768px) {
    .E-section {
      font-size: 13px;
    }
    .wrapper-text {
      background-size: 100%;
    }
  }
</style>
