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

    <div class="container-wrapper-benef">
      <div class="wrapper-benef">
        <span><i class="fa-solid fa-hourglass"></i></span>

        <p>
          Votre site E-commerce ou votre Application travaille pour vous 24h/24 et 7j/7. Une hyper-présence sur le net
          qui vous permet d'économisez du temps pour vous consacrer à d'autres tâches.
        </p>
      </div>
      <div class="wrapper-benef2 wrapper-benef">
        <span><i class="fa-solid fa-chart-line"></i></span>
        <p>Améliorez votre productivité  grâce au potentiel de votre outil digital. Votre application ou votre site inetrnet peut accomplir de mutilples tâches automatisées et ainsi augmenter considérablement votre productivité.</p>
      </div>
      <div class="wrapper-benef">
        <span><i class="fa-solid fa-sack-dollar"></i></span>
        <p>Augmentez vos revenus grâce à une visibilité acquise grâce à notre expertise SEO. + de visibilité + de prospects + plus de clients = plus d'argent!</p>
      </div>
    </div>
    <div class="wrapper-contact">
      <a class="contact" href="/#footer">Nous contacter</a>
      <a class="contact2" href="/#footer">Devis gratuit</a>
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
    grid-column: 2/12;
    grid-row: 1;
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
    font-weight: 900;
    color: rgb(223, 222, 222);
    font-family: epilogue;
    margin-top: 90px;
  }
  .container-wrapper-benef {
    grid-column: 1/13;
    grid-row: 2;
    display: flex;
    flex-direction: row;
    align-items: baseline;
    justify-content: space-between;
    margin-top: 50px;
    margin-bottom: 40px;
    gap: 20px;
    flex-wrap: wrap;
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
  }
  .wrapper-benef {
    display: flex;
    /* flex-direction: column; */
    width: auto;
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
    margin-bottom: 50px;
    text-align: left;
  }
  .contact {
    text-decoration: none;
    color: white;
    background-color: var(--CTA);
    font-family: kanit;
    font-weight: 400;
    margin-top: 0px;
    margin-left: 0px;
    width: 160px;
    border-radius: 6px;
    text-align: center;
    padding: 20px;
    box-shadow: 0px 0px 10px 2px rgba(76, 76, 76, 0.35);
  }
  .contact2 {
    text-decoration: none;
    color: white;
    background-image: linear-gradient(to left, var(--orange), var(--CTA));
    font-family: kanit;
    font-weight: 400;
    margin-top: 10px;
    margin-left: 10px;
    width: 160px;
    border-radius: 6px;
    text-align: center;
    padding: 20px;
    box-shadow: 0px 0px 10px 2px rgba(76, 76, 76, 0.35);
  }
  .contact:hover {
    animation: bounce 0.4s ease-in-out;
  }
  .contact2:hover {
    animation: bounce 0.4s ease-in-out;
  }
  .wrapper-contact {
    display: flex;
    gap: 0px;
    margin-top: 120px;
    align-items: baseline;
    justify-content: flex-start;
    margin-bottom: 100px;
  }

  @media only screen and (min-width: 300px) and (max-width: 768px) {
    .container-wrapper-benef {
      flex-direction: column;
    }
    .wrapper-benef2 {
      display: flex;
      flex-direction: column;
      width: 100%;
      align-items: flex-end;
      justify-content: flex-end;
      text-align: center;
      margin-top: 20px;
      padding: 10px;
      gap: 40px;
    }
    .wrapper-benef2 p {
      margin-top: 0px;
      font-size: var(--m);
      font-weight: 300;
      color: rgb(210, 210, 210);
      font-family: poppins;
      margin-bottom: 50px;
      text-align: right;
    }
  }
</style>
