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
    <div class="card linear-gradient">
            <a href="/Sites"><i class="fa-solid fa-desktop banner-icon icon"></i></a>
      <h3><strong>sites Internet</strong></h3>


      <!-- <a href="/Sites" class="button">+ d'infos</a> -->
    </div>
    <div class="card linear-gradient">
            <a href="/Applications"><i class="fa-solid fa-sitemap icon"></i></a>
      <h3><strong>Applications </strong></h3>


      <!-- <a href="/Sites" class="button">+ d'infos</a> -->
    </div>
  </div>

  <div class="wrapper-by-3-Cards">
    <div class="card linear-gradient">
            <a href="/Referencement"><i class="fa-solid fa-magnifying-glass-chart banner-icon icon"></i></a>

      <h3><strong>Référencement</strong></h3>

      <!-- <a href="/Sites" class="button">+ d'infos</a> -->
    </div>
    <div class="card linear-gradient">
            <a href="/Marketing"><i class="fa-solid fa-comments-dollar banner-icon icon"></i></a>

      <h3><strong>Marketing</strong></h3>

      <!-- <a href="/Sites" class="button">+ d'infos</a> -->
    </div>
  </div>

  <div class="wrapper-by-3-Cards">
    <div class="card linear-gradient">
      <h3><strong>Composants</strong></h3>
      <a href="/Composants"><i class="fa-solid fa-recycle icon"></i></a>

      <!-- <a href="/Sites" class="button">+ d'infos</a> -->
    </div>
    <div class="card linear-gradient">
       <h3><strong>Refonte</strong></h3>
            <a href="/Refonte"><i class="fa-solid fa-wand-magic-sparkles banner-icon icon"></i></a>

     

      <!-- <a href="/Sites" class="button">+ d'infos</a> -->
    </div>
  </div>
</div>

<style>
  .cont {
    background-color: transparent;
    grid-column: 1/12;
    grid-row: 3;
    margin-top: 70px;
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
    background-color: transparent;
    width: calc(40% - 50px);
    height: 200px;
    display: flex;
    flex-direction: column;
    align-items: center;
    justify-content: center;
    padding: 40px;
    gap: 20px;
    border-radius: 8px;
  }

.linear-gradient {
  border-style: solid;
  border-width: 1px;
  border-image: linear-gradient(to bottom,  var(--blue), var(--blue2) )1;

}

  .icon {
    color: transparent;
    -webkit-background-image: linear-gradient(to top, var(--blue2), var(--blue));
    background-image: linear-gradient(to top, var(--blue2), var(--blue));
    -webkit-background-clip: text;
    background-clip: text;
    font-size: 3em;
    z-index: 2;
  }
  .icon:hover {
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
    color: var(--colorC);
    font-weight: 300;
    font-size: var(--m);
    text-align: center;
  }

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
      width: 90%;
      height: auto;
      box-shadow: 3px 4px 15px rgba(0, 0, 0, 0.264);
      display: flex;
      flex-direction: column;
      align-items: center;
      justify-content: center;
      padding: 40px;

    }
  }
</style>
