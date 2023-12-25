<script>
  import ordi from "../Assets/png-gralypho/Other 03.png";
  import port from "../Assets/png-gralypho/Other 17.png";

</script>

<section class="A-section">
  <h1 >NOUS CRÉEONS LES OUTILS DIGITAUX QU'IL VOUS FAUT.</h1>
  <h2>Agence experte dans la création de site Web et dans le développement d’application.</h2>
  <img src={ordi} alt="Icon d'ornitateur en 3D" class="ordi" />
  <img src={port} alt="icon de téléphone portable en 3D" class="port" />
  <!-- <a class="link" href="/#sectionE">Découvrir</a> -->
  <div class="halo"></div>
</section>

<style>
  .A-section {
    display: grid;
    grid-template-columns: repeat(12, 1fr);
    grid-template-rows: auto;
    height: 100%;
    margin-top: 50px;
    font-size: 16px;
    background-color: var(--colorO);
  }
  .A-section h1 {
    word-wrap: break-word;
    grid-column: 2/10;
    grid-row: 1;
    margin-top: 20px;
    font-family: epilogue;
    font-weight: bolder;
    font-size: 2em;
    color: white;
  }
  .A-section h2 {
    word-wrap: break-word;
    grid-column: 2/8;
    grid-row: 1;
    margin-top: 150px;
    font-family: epilogue;
    font-weight: 300;
    font-size: 1em;
    color: var(--colorD);
  }
  .ordi {
    grid-column: 11;
    grid-row: 1;
    width: 140px;
    height: 140px;
    margin-top: 30px;
    margin-left: 20px;
    z-index: 2;
  }
  .port {
    grid-column: 11;
    grid-row: 1;
    width: 80px;
    height: 80px;
    transform: rotate(30deg);
    margin-top: 17px;
    margin-left: 10px;
    z-index: 3;
  }

  /* .link {
    grid-column: 2/6;
    grid-row: 1;
    display: flex;
    justify-content: center;
    align-items: center;
    width: auto;
    height: 3.3em;
    background-color: var(--colorA);
    border: none;
    border-radius: 40px;
    color: white;
    text-decoration: none;
    font-family: epilogue;
    font-weight: 400;
    font-size: 1em;
    margin-top: 220px;
    margin-bottom: 30px;
  } */

  .halo {
    grid-column: 11;
    grid-row: 1;
    background-color: rgb(79, 68, 235);
    width: 130px;
    height: 130px;
    border-radius: 50%;
    filter: blur(30px);
    z-index: 0;
    margin-left: 20px;
    margin-top: 40px;
  }

  @media screen and (max-width: 768px) {
    .A-section {
      font-size: 10px;
    }
  }
</style>
