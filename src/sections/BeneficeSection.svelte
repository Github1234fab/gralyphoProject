<script>
  import { onMount } from "svelte";
  import video from "../assets/video/web2.mp4";
</script>

<section class="section-benefices">
  <div class="container-benefices">
    <!-- +++++++++++++ -->
    <div class="wrapper-blocks">
      <h1>
        <span class="title-yellow">Automatisez</span> <br />
        votre outil digital. <i class="fa-solid fa-hourglass icon-difference"></i>
      </h1>
      <p>
        Votre site E-commerce ou votre Application travaille pour vous 24h/24 et 7j/7. Une hyper-présence sur le net qui
        vous permet d'économisez du temps pour vous consacrer à d'autres tâches.
      </p>
    </div>
    <!-- +++++++++++++ -->
    <div class="wrapper-blocks">
      <h1>
        <span class="title-yellow">Économisez</span> <br />
        du temps et de l'argent. <i class="fa-solid fa-chart-line icon-difference"></i>
      </h1>

      <p>
        Améliorez votre productivité grâce au potentiel de votre outil digital. Votre application ou votre site inetrnet
        peut accomplir de mutilples tâches automatisées et ainsi augmenter considérablement votre productivité.
      </p>
    </div>

    <!-- +++++++++++++ -->
    <div class="wrapper-blocks">
      <h1>
        <span class="title-yellow">Augmentez</span><br />
        votre potentiel client. <i class="fa-solid fa-sack-dollar icon-difference"></i>
      </h1>

      <p>
        Augmentez vos revenus grâce à une visibilité acquise grâce à notre expertise SEO. + de visibilité + de prospects
        + plus de clients = plus d'argent!
      </p>
    </div>
  </div>
</section>

<style>
  .section-benefices {
    display: flex;
    height: 600px;
    gap: 0px;
    background-color: var(--primary);
    align-items: center;
    justify-content: center;
    height: auto;
  }
  .container-benefices {
    margin-top: 100px;
    display: flex;
    flex-direction: row;
    height: auto;
    align-items: center;
    justify-content: center;
    margin-left: 50px;
    margin-right: 50px;
    gap: 20px;
  }
  .wrapper-blocks {
    display: flex;
    flex-direction: column;
    align-items: left;
    justify-content: left;
    width: 80%;
    min-height: 550px;
        max-height: 350px;
    box-shadow: 0px 0px 2px rgb(69, 68, 68);
     padding: 20px;
    margin-bottom: 100px;
  }
  .title-yellow {
    color: yellow;
    font-size: 2.2em;
    font-weight: 900;
    font-family: epilogue;
    letter-spacing: -1px;
  }
  .section-benefices h1 {
    font-size: var(--m);
    font-weight: 600;
    color: rgb(223, 222, 222);
    font-family: poppins;
  }
  .section-benefices p {
    font-size: var(--m);
    font-weight: 500;
    color: rgb(210, 210, 210);
    font-family: poppins;
    text-align: left;
    padding: 20px;
    margin-top: 20px;
    border-radius: 20px;
  }

  .icon-difference {
    font-weight: 600;
    margin-top: 10px;
    margin-left: 10px;
    color: transparent;
    font-size: 1.3em;
    -webkit-background-image: linear-gradient(to left, var(--orange) 40%, var(--blue));
    background-image: linear-gradient(to left, var(--orange) 40%, var(--blue));
    -webkit-background-clip: text;
    background-clip: text;
  }
</style>
