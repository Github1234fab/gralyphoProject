<script>
  import { onMount } from "svelte";

  onMount(() => {
    gsap.to(".section-ben", {
      opacity: 1,
      ease: "expoScale",
      scrollTrigger: {
        trigger: ".section-ben",
        start: "top 950px",
        end: "100px",
        scrub: 3,
      },
    });
  });
</script>

<section class="section-ben">
  <div class="wrapper-text-benefices">
    <h1>
      <div class="title-yellow">Automatisez</div>
      votre outil digital,
      <div class="title-yellow">Économisez</div>
      du temps et de l'argent,
      <div class="title-yellow">Augmentez</div>
      votre potentiel client.
    </h1>
  </div>

  <div class="container-wrapper-benef">
    <div class="wrapper-benef">
      <span><i class="fa-solid fa-hourglass"></i></span>
      <p>
        Votre site E-commerce ou votre Application travaille pour vous 24h/24 et 7j/7. Une hyper-présence sur le net qui
        vous permet d'économisez du temps pour vous consacrer à d'autres tâches.
      </p>
    </div>
    <div class="wrapper-benef2 wrapper-benef">
      <span><i class="fa-solid fa-chart-line"></i></span>
      <p>
        Améliorez votre productivité grâce au potentiel de votre outil digital. Votre application ou votre site inetrnet
        peut accomplir de mutilples tâches automatisées et ainsi augmenter considérablement votre productivité.
      </p>
    </div>
    <div class="wrapper-benef">
      <span><i class="fa-solid fa-sack-dollar"></i></span>
      <p>
        Augmentez vos revenus grâce à une visibilité acquise grâce à notre expertise SEO. + de visibilité + de prospects
        + plus de clients = plus d'argent!
      </p>
    </div>
  </div>
</section>

<style>
  .section-ben {
    display: grid;
    grid-template-columns: repeat(12, 1fr);
    grid-template-rows: auto;
    gap: 0px;
    background-color: var(--primary);
    /* align-items: center;
    justify-content: center; */
  }
  .wrapper-text-benefices {
    display: flex;
    gap: 0px;
    grid-column: 1/12;
    grid-row: 1;
    margin-left: 50px;
  }
  .title-yellow {
    color: yellow;
    font-size: var(--xl);
    font-weight: 900;
    font-family: epilogue;
    letter-spacing: -1px;
  }
  .section-ben h1 {
    font-size: var(--xl);
    font-weight: 800;
    color: rgb(223, 222, 222);
    font-family: epilogue;
    margin-top: 100px;
  }
  .container-wrapper-benef {
    grid-column: 1/12;
    grid-row: 2;
    display: flex;
    flex-direction: row;
    margin-top: 50px;
    margin-bottom: 100px;
    margin-left: 100px;
    margin-right: 100px;
    gap: 20px;
  }
  .section-ben span {
    height: 120px;
    width: 120px;
    border-radius: 20%;
    font-family: poppins;
    letter-spacing: -2px;
    font-weight: 600;
    color: transparent;
    font-size: 3em;
    -webkit-background-image: linear-gradient(to left, var(--orange) 40%, var(--blue));
    background-image: linear-gradient(to left, var(--orange) 40%, var(--blue));
    -webkit-background-clip: text;
    background-clip: text;
    margin-left: -30px;
  }
  .wrapper-benef {
    display: flex;
    flex-direction: column;
    min-width: 200px;
    min-height: 300px;
    align-items: flex-start;
    justify-content: flex-start;
    text-align: center;
    margin-top: 20px;
    padding: 30px;
    gap: 40px;
    border: 1px grey solid;
    border-radius: 20px;
  }

  .wrapper-benef p {
    margin-top: 0px;
    font-size: var(--m);
    font-weight: 300;
    color: rgb(210, 210, 210);
    font-family: poppins;
    text-align: left;
    margin-top: -60px;
  }

  @media only screen and (min-width: 300px) and (max-width: 768px) {
    .container-wrapper-benef {
      grid-column: 1/13;
      flex-direction: column;
      display: flex;
      margin-top: 50px;
      margin-bottom: 100px;
      gap: 20px;
      align-items: center;
      justify-content: center;
      align-self: center;
    }
    .wrapper-benef {
      display: flex;
      flex-direction: column;
      min-width: calc(400px - 20px);
      text-align: center;
      margin-top: 20px;
      padding: 10px;
      gap: 40px;
    }
      .wrapper-text-benefices {
    display: flex;
    gap: 0px;
    grid-column: 1/13;
    grid-row: 1;
    margin-left: 20px;
  }
    .section-ben span {
    margin-left: -30px;
  }
  }
</style>
