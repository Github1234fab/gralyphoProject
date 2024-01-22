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
  import circle from "../Assets/png-gralypho/circleOne.svg";
  import circleOne from "../Assets/png-gralypho/brutalism/Frame (15).png";
  import circleTwo from "../Assets/png-gralypho/brutalism/Frame (16).png";
  import circleThree from "../Assets/png-gralypho/circlePrismThree.svg";
  import circleFour from "../Assets/png-gralypho/brutalism/Group.png";
  import { onMount } from "svelte";

  onMount(() => {
    gsap.to(".circleOne", {
      rotate: 1440,
      scrollTrigger: {
        trigger: ".circleOne",
        start: "top 700px",
        end: "300px",
        scrub: 3,
        repeat: 3,
      },
    });
  });
  onMount(() => {
    gsap.to(".circleTwo", {
      rotate: 360,
      scrollTrigger: {
        trigger: ".circleTwo",
        start: "top 700px",
        end: "300px",
        scrub: 1,
        repeat: 3,
      },
    });
  });
  onMount(() => {
    gsap.to(".circleThree", {
      rotate: 360,
      scrollTrigger: {
        trigger: ".circleThree",
        start: "top 700px",
        end: "300px",
        scrub: 1,
        repeat: 3,
      },
    });
  });
  onMount(() => {
    gsap.to(".circleFour", {
      rotate: 360,
      scrollTrigger: {
        trigger: ".circleFour",
        start: "top 700px",
        end: "300px",
        scrub: 1,
        repeat: 3,
      },
    });
  });
</script>

<Header />
<section class="A-section">
  <h1>Chez <span>Gralypho</span>, <br />nous transformons l'ordinaire en <br /> extraordinaire !</h1>
  <h2>
    <!-- Augmentez votre visibilité, simplifiez vos opérations <br />et offrez à vos clients <br />une expérience <br>
    exceptionnelle ! -->
      Augmentez votre visibilité, simplifiez vos opérations <br />et touchez plus de clients.
  </h2>
  <div class="wrapper-link">
  <a class="link" href="/#sectionE">Découvrir</a>
  </div>
  <!-- <img src={circleOne} alt="cercle décoré" class="circleOne opacity-circle" /> -->
  <!-- <img src={circleFour} alt="cercle décoré" class="circleTwo opacity-circle"> -->
  <!-- <img src={circleThree} alt="cercle décoré" class="circleThree"> -->
  <!-- <img src={circleTwo} alt="cercle décoré" class="circleFour opacity-circle"> -->
</section>

<style>
  .A-section {
    display: grid;
    grid-template-columns: repeat(12, 1fr);
    grid-template-rows: 0.333fr  0.333fr  0.333fr;
height: 100vh;
    font-size: 16px;
    z-index: 1;
    background-color: var(--primary);
  }
  .A-section h1 {
    z-index: 1;
    text-align: left;
    font-family: epilogue;
    font-weight: 900;
    font-size: clamp(2.2rem, 8vw, 5rem);
    color: white;
    grid-column: 2/13;
    grid-row: 1;
    margin-top: 50px;
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
    font-weight: 200;
    text-align: left;
    font-size: clamp(1.2rem, 8vw, 1.3rem);
    color: var(--colorC);
    grid-column: 2/12;
    grid-row: 2;
    margin-top: 0px;
  }
  .wrapper-link{
       grid-column: 9/12;
    grid-row: 3;
  }

  .link {
    display: flex;
     justify-content: center;
    align-items: center;
    z-index: 3;
    border-radius: 8px;
    color: white;
    text-decoration: none;
    font-family: epilogue;
    font-weight: 400;
    font-size: clamp(1.1rem, 8vw, 1.4rem);
    border: solid #2993fa 2px;
    transition: 0.4s ease-in-out;
    padding: 30px;
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
@media screen and (max-width: 768px){
 .A-section h1{
    grid-column: 1/12;
    grid-row: 1;
    margin-left: 40px;
 }
 .A-section h2{
    grid-column: 1/12;
    grid-row: 2;
    margin-left: 40px;
 }
  .wrapper-link{
    grid-column: 7/12;
    grid-row: 3;
  }
  .link{
    font-size: 1.2em;
  }
}
</style>
