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
  import circle from"../Assets/png-gralypho/circleOne.svg";
  import circleOne from"../Assets/png-gralypho/circlePrismOne.svg";
  import circleTwo from"../Assets/png-gralypho/circlePrismTwo.svg";
  import circleThree from"../Assets/png-gralypho/circlePrismThree.svg";
    import circleFour from"../Assets/png-gralypho/circlePrismFour.svg";
import { onMount } from "svelte";
  
  onMount(() => {
    gsap.to(".circleOne", {
      rotate: 360,
      scrollTrigger: {
        trigger: ".circleOne",
        start: "top 700px",
        end: "300px",
        scrub: 3  ,
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
        scrub: 3  ,
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
        scrub: 3  ,
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
        scrub: 3  ,
   repeat: 3, 
      },
    });
  });

</script>


  <Header />
<section class="A-section">


    <h1>Chez <span>Gralypho</span>, <br />nous transformons l'ordinaire <br /> en extraordinaire !</h1>
    <h2>
      Augmentez votre visibilité, simplifiez vos opérations et offrez à vos clients une expérience exceptionnelle !
    </h2>
    <a class="link" href="/#sectionE">Découvrir</a>
<img src={circleOne} alt="cercle décoré" class="circleOne opacity-circle">
<img src={circleTwo} alt="cercle décoré" class="circleTwo opacity-circle">
<!-- <img src={circleThree} alt="cercle décoré" class="circleThree"> -->
<img src={circleFour} alt="cercle décoré" class="circleFour opacity-circle">

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
  .A-section h1 {
    z-index: 1;
    text-align: left;
    font-family: epilogue;
    font-weight: 900;
    font-size: 2.8em;
    color: white;
    line-height: 56px;
    margin-top: 60px;
    grid-column: 2/13;
    grid-row: 1;
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
    margin-top: 40px;
     grid-column: 2/12;
    grid-row: 2;
  }

  .link {
     grid-column: 2/12;
    grid-row: 3;
    display: flex;
    z-index: 3;
    justify-content: center;
    align-items: center;
    width: 150px;
    height: 3.1em;
    border-radius: 8px;
    color: white;
    text-decoration: none;
    font-family: epilogue;
    font-weight: 600;
    font-size: 1em;
    box-shadow: inset 2px 2px 5px var(--colorO);
background-color:  var(--blue);
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
  .circleOne{
    grid-column: 9;
    grid-row: 3;
    height: 100px;
    z-index: 0;
    margin-top: 30px;
  }
    .circleTwo{
    grid-column: 10;
    grid-row: 1;
    height: 100px;
    z-index: 0;
    margin-top: 30px;
  }

    .circleFour{
    grid-column: 7;
    grid-row: 3;
    height: 100px;
    z-index: 0;
    margin-top: 20px;
  }
  .opacity-circle{
    opacity: 0.8;
  }

  @media screen and (max-width: 768px) {
   
    .A-section {
      font-size: 14px;
    }
    .A-section h1 {
      z-index: 1;
      text-align: left;
      font-family: epilogue;
      font-weight: 900;
      font-size: 2.8em;
      color: white;
      line-height: 56px;
      margin-left: 20px;
      margin-top: 40px;
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
      margin-left: 20px;
      margin-top: 20px;
    }
    .link {
      margin-left: 20px;
      margin-top: 50px;
      margin-bottom: 100px;
    }
  }
</style>
