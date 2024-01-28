<script>
  import billy from "../Assets/png-gralypho/Billy 33.png";
  import billy2 from "../Assets/png-gralypho/Billy 52.png";
  import billy3 from "../Assets/png-gralypho/Billy 53.png";
  import billy4 from "../Assets/png-gralypho/Billy 56.png";
</script>

<div class="action-section">
  <div class="wrapper-text">
    <h1>Prêt à démarrer <br /> votre <span>projet ?</span></h1>
    <h2>
      Découvrez comment nous pouvons renforcer votre marque, <br /> améliorer votre visibilité, <br /> et générer des résultats
      tangibles.
    </h2>
  </div>
  <div class="wrapper-action">
    <div class="card-action">
      <div class="wrapper-img">
        <img src={billy4} alt="" class="billy" />
      </div>
      <h3>Captez</h3>
      <p>
        Boostez votre visibilité en ligne et captez l'attention de vos prospects potentiels. Grâce à des stratégies
        numériques efficaces et une présence web percutante, nous mettons en avant votre entreprise là où se trouvent
        vos clients.
      </p>
    </div>
    <div class="card-action">
      <div class="wrapper-img">
        <img src={billy} alt="" class="billy" />
      </div>
      <h3>Optimisez</h3>
      <p>
        Optimisez votre présence en ligne avec des sites web performants et conviviaux. Nous travaillons sur
        l'optimisation de votre site pour garantir une expérience utilisateur exceptionnelle et assurer que vos futurs
        clients trouvent rapidement et facilement les informations dont ils ont besoin.
      </p>
    </div>
    <div class="card-action">
      <div class="wrapper-img">
        <img src={billy3} alt="" class="billy" />
      </div>
      <h3>Gagnez</h3>
      <p>
        Gagnez en ventes, en visibilité et en influence grâce à une stratégie de marketing digital bien élaborée. Notre
        approche centrée sur le client vous permet de conquérir de nouveaux marchés, fidéliser votre clientèle et
        augmenter vos résultats en ligne. Ensemble, gagnons le succès digital !
      </p>
    </div>
  </div>

    <a href="#contact" class="cta-button">Commencez <br />votre <br /> aventure digitale</a>

</div>

<style>
  .action-section {
    display: grid;
    grid-template-columns: repeat(12, 1fr);
    grid-template-rows: auto;
    height: auto;
  }
  .wrapper-text {
    grid-column: 1/12;
    grid-row: 1;
    display: flex;
    width: 100%;
    flex-direction: column;
    gap: 20px;
    margin-top: 50px;
    margin-left: 20px;
  }
  .wrapper-text h1 {
    font-size: var(--xl);
    font-weight: 900;
    color: white;
    font-family: Epilogue;
    margin-left: 20px;
  }
  .wrapper-text h1 span {
    color: transparent;
    -webkit-background-image: linear-gradient(to left, var(--orange), var(--blue));
    background-image: linear-gradient(to left, var(--orange), var(--blue));
    -webkit-background-clip: text;
    background-clip: text;
  }
  .wrapper-text h2 {
    font-size: var(--l);
    font-weight: 300;
    color: white;
    font-family: epilogue;
        margin-left: 20px;
  }
  .wrapper-action {
    grid-column: 2/12;
    grid-row: 2;
    display: flex;
    justify-content: center;
    align-items: center;
    gap: 0px;
    
  }
  .card-action {
    display: flex;
    flex-direction: column;
    justify-content: left;
    align-items: left;
    gap: 20px;
    width: 100%;
    max-width: 350px;
    padding: 20px;
    color: white;

  }
  .card-action h3 {
    font-size: var(--l);
    font-weight: 600;
    color: var(--colorC);
    font-family: epilogue;
  }
  .card-action p {
    font-size: var(--m);
    font-weight: 300;
    color: var(--colorC);
    font-family: epilogue;
  }
  .wrapper-img {
    width: 100%;
    max-width: 150px;
    height: 100%;
    max-height: 150px;
    display: flex;
    justify-content: left;
    align-items: left;
  }
  .billy {
    width: 100%;
    max-width: 100px;
    height: 100%;
    max-height: 100px;
  }
  
  .cta-button {
          grid-column: span 12;
          margin-right: 500px;
          margin-left: 500px;
    border-radius: 8px;
    background-color: var(--ca);
    color: white;
    font-size: var(--m);
    font-weight: 400;
    text-decoration: none;
    padding: 20px;
    text-align: center;
  }

  @media screen and (max-width: 768px) {
    .wrapper-action {
      flex-direction: column;
      gap: 50px;
    }
  }
</style>
