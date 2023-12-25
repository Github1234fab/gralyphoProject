<script>
  import Robot from "../Assets/png-gralypho/Saly-39.png";
  import { onMount } from "svelte";

  //   onMount(() => {
  //     gsap.to(".robot", {
  // rotate: 360,
  //       scale: 0.9,
  // //      ease: "elastic.out(1,0.3)",
  //       scrollTrigger: {
  //         trigger: ".robot",
  //         start: "top 500px",
  // 	end: "-200px",
  // 	scrub: 2,
  //       },
  // })
  //   });

  onMount(() => {
    gsap.to(".robot", {
      scale: 1.1,
      ease: "expoScale",
      scrollTrigger: {
        trigger: ".robot",
        start: "top 500px",
        end: "-200px",
        scrub: 2,
      },
    });
  });
</script>

<section class="C-section">
  <img src={Robot} alt="icon de robot en 3D" class="robot" />
  <h1>Votre projet est unique et mérite une technologie appropriée.</h1>
  <h2>
    Selon vos besoins spécifiques, nous choisirons méticuleusement la technologie la plus adaptée pour la réalisation de
    votre application.
  </h2>
  <p>
    Wordpress? Wix? Shopify? From Scratch? Woo Commerce? Squarespace ? Webflow? (...) Quelle est la technologie la plus
    appropriée à la réalisation de votre site internet ou de votre application? C'est une question fondamentale parce
    qu'elle va déterminer la durée de conception, le coût et l'efficacité de votre outil en terme de rapidité, de
    fonctionnalité et de maintenance
  </p>
  <div class="halo"></div>
</section>

<style>
  .C-section {
    display: grid;
    grid-template-columns: repeat(12, 1fr);
    grid-template-rows: 1;
    height: 600px;
    font-size: 16px;
    background-color: var(--colorO);
    margin-top: 100px;
  }
  .C-section h1 {
    word-wrap: break-word;
    grid-column: 6/12;
    grid-row: 1;
    margin-left: 20px;
    font-family: epilogue;
    font-weight: 600;
    font-size: 1.8em;
    color: white;
    text-transform: uppercase;
  }
  .C-section h2 {
    grid-column: 6/12;
    grid-row: 1;
    margin-left: 20px;
    margin-top: 130px;
    font-family: epilogue;
    font-weight: 100;
    font-size: 1.2em;
    color: var(--colorC);
  }
  .C-section p {
    grid-column: 2/12;
    grid-row: 1;
    color: var(--colorC);
    margin-top: 300px;
    text-align: justify;
    font-weight: 300;
    font-size: 1.1em;
  }
  .robot {
    transform: rotate(0deg);
    transform: scale(0.7);
    grid-column: 2/7;
    grid-row: 1;
    height: 180px;
    width: 180px;
    margin-left: -10px;
    margin-top: 0px;
    z-index: 1;
  }
  .halo {
    grid-column: 2/7;
    grid-row: 1;
    background-color: rgb(79, 68, 235);
    width: 100px;
    height: 100px;
    border-radius: 50%;
    filter: blur(30px);
    z-index: 0;
    margin-left: 30px;
    margin-top: 50px;
  }
  @media screen and (max-width: 801px) {
    .C-section {
      font-size: 11px;
      height: 400px;
    }
    .C-section h2 {
      margin-top: 80px;
    }
    .C-section p {
      margin-top: 230px;
    }
  }
  @media screen and (max-width: 560px) {
    .C-section {
      font-size: 11px;
      height: 600px;
    }
    .C-section h2 {
      margin-top: 150px;
    }
    .C-section p {
      margin-top: 300px;
    }
    .robot {
      height: 160px;
      width: 160px;
    }
  }
</style>
