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
      <h3>Sites Web</h3>
      <a href="/Sites"><i class="fa-solid fa-arrow-right arrow"></i></a>
    </div>
    <div class="card">
      <i class="fa-solid fa-sitemap icon"></i>
      <h3>Applications</h3>
      <a href="/Applications"><i class="fa-solid fa-arrow-right arrow"></i></a>
    </div>
  </div>

  <div class="wrapper-by-3-Cards">
    <div class="card">
      <i class="fa-solid fa-magnifying-glass-chart banner-icon icon"></i>
      <h3>Référencement</h3>
      <a href="/Referencement"><i class="fa-solid fa-arrow-right arrow"></i></a>
    </div>
    <div class="card">
      <i class="fa-solid fa-comments-dollar banner-icon icon"></i>
      <h3>Marketing</h3>
      <a href="/Marketing"><i class="fa-solid fa-arrow-right arrow"></i></a>
    </div>
  </div>

  <div class="wrapper-by-3-Cards">
    <div class="card">
      <i class="fa-solid fa-recycle icon"></i>
      <h3>Composants</h3>
      <a href="/Composants"><i class="fa-solid fa-arrow-right arrow"></i></a>
    </div>
    <div class="card">
      <i class="fa-solid fa-wand-magic-sparkles banner-icon icon"></i>
      <h3>Refonte</h3>
      <a href="/Refonte"><i class="fa-solid fa-arrow-right arrow"></i></a>
    </div>
  </div>
</div>

<style>
  .cont {
    background-color: transparent;
    grid-column: 2/12;
    grid-row: 2;
    margin-top: 50px;
    margin-bottom: 50px;
    gap: 40px;
    display: flex;
    flex-direction: column;
    align-items: center;
    justify-content: center;
  }
  .wrapper-by-3-Cards {
    display: flex;
    justify-content: center;
    gap: 40px;
    flex-wrap: wrap;
    width: 100%;
  }

  .card {
    z-index: 0;
    background-color: transparent;
    width: 30%;
    height: auto;
    box-shadow: 3px 4px 15px rgba(0, 0, 0, 0.264);
    display: flex;
    flex-direction: column;
    align-items: center;
    justify-content: center;
    padding: 40px;
    gap: 30px;
  }
  .card:hover {
    background-color: var(--colorL);
  }
  .icon {
    color: var(--colorN);
    font-size: 1.9em;
  }
  .arrow {
    z-index: 2;
    color: var(--colorA);
    font-size: 2em;
    transition: 0.1s ease-in-out;
  }
  .arrow:hover {
    transform: scale(1.3);
  }
  .card h3 {
    font-family: kanit;
    color: white;
    font-weight: 400;
    font-size: 1.3em;
    text-align: center;
  }

  @media screen and (max-width: 800px) {
    .wrapper-by-3-Cards {
      display: flex;
      align-items: center;
      justify-content: center;
      flex-direction: column;
      gap: 40px;
      flex-wrap: wrap;
      width: 100%;
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
      gap: 30px;
      border: 1px solid grey;
    }
  }
</style>
