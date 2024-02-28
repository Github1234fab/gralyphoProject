<script>
  import { fade, slide } from "svelte/transition";
  // import bg from "../../Assets/png-gralypho/41.png";
  import Header from "../../sections/Header.svelte";
</script>

<Header />
<section class="" in:fade={{ duration: 3000 }}>
  <div class="wrapper background-animated">
    <h1>Refonte</h1>
    <!-- <img src={bg} alt="" class="bg" /> -->

    <p>
     <span><strong>REFONTE ?!</strong><br><br> </span>
Le terme refonte signifie un relooking de votre site actuel!<br> <br>
     Il y a des modes, des courants, des tendances, des styles, des couleurs, des formes, des typographies, des images, des animations, des effets, des transitions, des sons, des vidéos, des illustrations, des photos, des dessins, des graphiques, des logos, des icônes, des boutons, des menus (...)  qui évoluent avec le temps. <br><br>
     Et parfois votre site web est un peu dépassé, voir obsolète. Alors, plutôt que de refaire un site de A à Z, il peut être pus intéressant et moins onéreux de le relooker, de le refondre, de le moderniser, de le mettre au goût du jour. <br><br>
    </p>

    <h4>
      Vous êtes intéressé par une refonte ou vous souhaitez en savoir d'avantage? <br>Alors parlons en ensemble autour d'un petit café.
    </h4>
    <div class="wrapper-contact">
      <a href="mailto:gralypho@gmail.com " class="contact"><i class="fa-regular fa-envelope"></i></a>
      <a href="tel:0672901614" class="contact"><i class="fa-solid fa-phone-volume"></i></a>
      <a href="tel:0672901614" class="contact"><i class="fa-solid fa-mug-hot"></i></a>

    </div>
  </div>
</section>

<style>
  .wrapper-contact {
    display: flex;
    gap: 30px;
    justify-content: center;
    align-items: center;
    margin-top: 50px;
  }
  h4 {
    z-index: 2;
    margin-top: 30px;
    color: var(--colorC);
    text-align: left;
    line-height: 30px;
    font-weight: 400;
    font-size: 1.2em;
    font-family: epilogue;
    text-align: center;
  }
  a {
    border: 2px solid var(--blue);
    padding: 20px;
    border-radius: 10px;
    font-size: 2em;
    color: var(--colorC);
    z-index: 2;
  }
  a:hover {
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
  section {
    display: grid;
    grid-template-columns: repeat(12, 1fr);
    grid-template-rows: auto;
    /* background-color: var(--colorO); */
    height: 100%;
    width: 100%;
    margin-top: 30px;
    margin-bottom: 50px;

  }
  .wrapper {
    grid-column: 1/13;
    grid-row: 1;
    display: flex;
    flex-direction: column;
    justify-content: left;
    align-items: left;
    height: 100%;
    position: relative;
    padding: 30px;
  }
  .wrapper::after {
    position: absolute;
    content: "";
    background-color: #1a1c2186;
    top: 0;
    left: 0;
    right: 0;
    bottom: 0;
  }
  section h1 {
    z-index: 2;
    text-align: left;
    font-family: Kanit;
    font-weight: 600;
    font-size: var(--xl);
    color: white;
    margin-top: 50px;
    line-height: 37px;
  }
  section p span {
    z-index: 2;
    color: white;
    font-size: var(--l);
    font-weight: 400;
    text-align: left;
    line-height: 30px;
    margin-top: 30px;
    font-family: kanit;
  }
  section p {
    z-index: 2;
    margin-top: 30px;
    color: var(--colorC);
    text-align: left;
    line-height: 30px;
    font-weight: 300;
    font-size: var(--m);
    font-family: epilogue;
  }
  
</style>
