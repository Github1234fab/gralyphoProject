<script>
  import { fade, slide } from "svelte/transition";
  import bg from "../../Assets/png-gralypho/41.png";
</script>

<section class="" in:fade={{ duration: 3000 }}>
  <div class="container">
    <div class="wrapper">
      <h1>Sites Web</h1>
      <img src={bg} alt="" class="bg">
      <p>
        <span>Qu'est-ce qu'une application?</span> <br /><br />
        Une application est un logiciel qui permet de réaliser une tâche spécifique. <br /><br /> Voilà princpalement la
        différence entre une application et un site web. Le site web traite d'un sujet et le développe à travers ses
        différentes rubriques, ses différentes pages et ses différentes fonctionnalités. <br /><br /> Une application va
        donc, quant à elle, permettre à l'utilisateur de réaliser une tâche spécifique. <br /> <br />Par exemple, une
        application de gestion de stock, une application de gestion de planning, de gestion de facturation, un
        application météorologique, de rencontre, de localisation, etc. <br /><br />
        <span>Quel est le budget pour obtenir une application?</span> <br /><br />
        Le budget va varier d'une application à l'autre en fonftion des besoins qu'elle requiert et de la complexité de sa
        réalisation. <br /><br /> Il est donc difficile de donner un prix fixe pour une application. <br /><br />
        Cependant, nous pouvons vous donner une fourchette de prix pour une application simple, sans base de données, ni
        gestion comlexe, le tarif peut débuter autour de 2000 euros et aller jsuqu'à 10 000 euros et plus.
        <br /><br />
        <span>Quels sont les délais de création?</span> <br /><br />
        Nous pouvons concevoir et réaliser une application entre 1 mois et un an, selon sa complexité !<br /><br /> Il
        est essentiel de déterminer votre projet dans les moindres détails, car les prix peuvent considérablement varier
        en fonction des fontionnalités, des besoins<br /><br /> Cependant, nous pouvons vous donner une fourchette de prix
        pour une application simple, sans base de données, ni gestion comlexe, le tarif peut débuter autour de 2000 euros
        et aller jsuqu'à 10 000 euros et plus.
      </p>
    </div>
  </div>
</section>

<style>
  section {
    display: grid;
    grid-template-columns: repeat(12, 1fr);
    grid-template-rows: auto;
    background-color: var(--colorO);
    height: 100%;
    width: 100%;
    margin-top: 30px;
    margin-bottom: 50px;
  }
  .container {
    z-index: 0;
    position: relative;
    grid-column: 2/12;
    grid-row: 1;
    display: grid;
    grid-template-columns: repeat(12, 1fr);
    grid-template-rows: 1;
    border-radius: 20px;
    padding: 20px;
    border: solid 1px rgb(55, 55, 55);
    height: 100%;
    /* background-image: url(../../Assets/png-gralypho/qqquad.svg); */
  }
  .container::after {
        border-radius: 20px;
        z-index: 1;
    position: absolute;
    content: "";
    background-color: rgba(12, 12, 27, 0.66);
    top: 0;
    left: 0;
    right: 0;
    bottom: 0;
    width: 100%;
    height: 100%;
  }
  .wrapper {
    grid-column: 2/12;
    grid-row: 1;
    display: flex;
    flex-direction: column;
    justify-content: left;
    align-items: left;
    height: 100%;
    background-image: url(../../Assets/png-gralypho/rrrainbow.svg);
  }
  section h1 {
            z-index: 2;
    word-wrap: break-word;
    text-align: left;
    font-family: epilogue;
    font-weight: 500;
    font-size: 1.7em;
    color: white;
    margin-top: 50px;
    line-height: 37px;
  }
  section p span {
           z-index: 2;
    color: white;
    font-size: 1.2rem;
    font-weight: 500;
    text-align: left;
    line-height: 30px;
    margin-top: 30px;
  }
  section p {
           z-index: 2;
    margin-top: 30px;
    color: var(--colorC);
    text-align: left;
    line-height: 30px;
    font-weight: 300;
    font-size: 1.1em;
    font-family: epilogue;
  }
  .bg{
    z-index: 2;
    margin-top: 30px;
    border-radius: 20px;
  }
</style>
