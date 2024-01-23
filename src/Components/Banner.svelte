<script>
  import { onMount } from "svelte";

  onMount(() => {
    const timeline = gsap.timeline();

    // Utilisez le sélecteur de classe directement
    timeline.to(".banner-icon", {
      opacity: 1,
      y: 0,
      stagger: 0.2,
      duration: 0.5,
      scrollTrigger: {
        trigger: ".banner-icon", // Utilisez le sélecteur de classe ici aussi
        start: "top 3500px",
        // end: "-300px",
        scrub: 1,
      },
    });
  });
</script>

<div class="cont">
  <div class="wrapper-by-3-Cards">
    <div class="card">
      <i class="fa-solid fa-desktop banner-icon icon"></i>
      <h3>Création de <strong>sites Internet</strong></h3>
      <!-- <a href="/Sites" class="button">+ d'infos</a> -->
    </div>
    <div class="card">
      <i class="fa-solid fa-sitemap icon"></i>
      <h3>Développement d'<strong>Applications </strong></h3>
    <!-- <a href="/Sites" class="button">+ d'infos</a> -->
    </div>
  </div>

  <div class="wrapper-by-3-Cards">
    <div class="card">
      <i class="fa-solid fa-magnifying-glass-chart banner-icon icon"></i>
      <h3><strong>Référencement</strong></h3>
    <!-- <a href="/Sites" class="button">+ d'infos</a> -->
    </div>
    <div class="card">
      <i class="fa-solid fa-comments-dollar banner-icon icon"></i>
      <h3><strong>Marketing & Communication</strong></h3>
<!-- <a href="/Sites" class="button">+ d'infos</a> -->
    </div>
  </div>

  <div class="wrapper-by-3-Cards">
    <div class="card">
      <i class="fa-solid fa-recycle icon"></i>
      <h3><strong>Composants Web</strong></h3>
<!-- <a href="/Sites" class="button">+ d'infos</a> -->
    </div>
    <div class="card">
      <i class="fa-solid fa-wand-magic-sparkles banner-icon icon"></i>
      <h3><strong>Refonte</strong></h3>
  <!-- <a href="/Sites" class="button">+ d'infos</a> -->
    </div>
  </div>
</div>

<style>
  .cont {
    background-color: transparent;
    grid-column: 1/12;
    grid-row: 3;
    margin-top: 80px;
    margin-bottom: 50px;
    /* gap: 60px; */
    display: flex;
    flex-direction: column;
    align-items: center;
    justify-content: center;
        gap: 10px;
  }
  .wrapper-by-3-Cards {
    display: flex;
    justify-content: center;
    flex-wrap: wrap;
    width: 100vw;
     gap: 10px;
  }
  .card {
    z-index: 0;
    background-color: var(--colorC);
    width: calc(100% - 50px);
    height: 400px;
    /* box-shadow: 3px 4px 25px rgba(0, 0, 0, 0.27); */
    display: flex;
    flex-direction: column;
    align-items: center;
    justify-content: center;
    padding: 40px;
    gap: 100px;
  
  }
  /* .button{
    color: white;
text-decoration: none;
font-weight: 400;
font-size: 1em;
height: auto;
border-radius: 8px;
background-color: var(--blue);
padding: 12px;
font-family: kanit;
  }
  .button:hover{
    animation: bounce 0.4s ease-in-out;
  } */
  .icon {
    color: transparent;
   background-image: linear-gradient(to bottom, var(--primary) , var(--blue) 50%);
   background-clip: text;
    font-size: 9em;
    z-index: 2;

  }
  .icon:hover{
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
  .card h3 {
    font-family: epilogue;
    color: var(--primary);
    font-weight: 800;
    font-size: var(--l);
    text-align: center;
  }
/* 
  @media screen and (max-width: 800px) {
    .wrapper-by-3-Cards {
      display: flex;
      align-items: center;
      justify-content: center;
      flex-direction: column;
      flex-wrap: wrap;
      width: 100vw;
    }
    .card {
      z-index: 0;
      background-color: transparent;
      width: 100vw;
      height: auto;
      box-shadow: 3px 4px 15px rgba(0, 0, 0, 0.264);
      display: flex;
      flex-direction: column;
      align-items: center;
      justify-content: center;
      padding: 40px;
      border: 1px solid grey;
    }
  } */
</style>
