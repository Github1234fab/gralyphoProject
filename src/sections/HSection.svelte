<script>
  import Climber from "../Assets/png-gralypho/Saly-15.png";
  import six from "../Assets/png-gralypho/six.svg";
  import Header from "../sections/Header.svelte";

  import { onMount } from "svelte";

  onMount(() => {
    gsap.to(".gsap5", {
      rotation: 730,
      duration: 2,
      scrub: 3,
    });
  });
</script>

<Header />
<section class="H-section">
  <div class="wrapper-png">
    <img src={Climber} alt="" class="climb gsap5" />
    <img src={six} alt="" class="six gsap5" />
  </div>
  <div class="wrapper-text">
    <h1><span>Gralypho</span></h1>
    <h2><span>Expertise </span>et <span>Expérience </span><br />Votre victoire Digitale assurée !</h2>
  </div>
  <div class="wrapper-contact">
    <a href="/#footer">Nous contactez</a>
  </div>
</section>

<style>
  .H-section {
    display: flex;
    flex-direction: column;
    height: 100vh;
    font-size: 16px;
    opacity: 1;
    justify-content: center;
    align-items: center;
    gap: 30px;
  }
  .wrapper-png {
    display: grid;
    grid-template-columns: repeat(4, 1fr);
    grid-template-rows: 1;
    margin-top: -140px;
  }
  .climb {
    grid-column: 6 / span 6;
    grid-row: 1;
    height: 160px;
    z-index: 2;
    align-self: center;
  }
  .six {
    grid-column: 6 / span 6;
    grid-row: 1;
    height: 115px;
    z-index: 1;
    margin-top: 90px;
  }
  .wrapper-text {
    display: flex;
    flex-direction: column;
    border-radius: 20px;
  }
  .H-section h1 {
    text-align: center;
    font-family: epilogue;
    font-weight: 600;
    font-size: var(--xl);
    color: white;
  }
  .H-section h1 span {
    font-weight: 900;
    color: transparent;
    -webkit-background-image: linear-gradient(to left, var(--orange), var(--blue));
    background-image: linear-gradient(to left, var(--orange), var(--blue));
    -webkit-background-clip: text;
    background-clip: text;
  }
  .H-section h2 {
    font-family: epilogue;
    font-weight: 300;
    font-size: var(--l);
    color: white;
    text-align: center;
    line-height: 30px;
    padding: 20px;
  }
  .H-section h2 span {
    font-weight: 600;
    color: white;
  }

  .wrapper-contact {
    display: flex;
    flex-direction: column;
    align-items: center;
    justify-content: center;
    background-color: var(--bg);
    height: auto;
    padding: 20px;
    text-align: center;
    border-radius: 4px;
    gap: 10px;
    background-color: var(--ca);
  }
  .wrapper-contact:hover {
    animation: bounce 0.4s ease-in-out;
  }

  .wrapper-contact a {
    text-decoration: none;
    color: var(--colorC);
    font-family: kanit;
    font-weight: 400;
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
  .gsap5 {
    background-color: transparent;
  }
</style>
