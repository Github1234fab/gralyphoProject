<script>
  import { onMount } from "svelte";

  function shuffleArray(array) {
    for (let i = array.length - 1; i > 0; i--) {
      const j = Math.floor(Math.random() * (i + 1));
      [array[i], array[j]] = [array[j], array[i]];
    }
  }

  function randomColorCarte() {
    const randomComponent = () => Math.floor(Math.random() * 256);
    const color = `rgb(${randomComponent()}, ${randomComponent()}, ${randomComponent()})`;
    return color;
  }

  onMount(() => {
    let cards = Array.from(document.querySelectorAll(".carte"));
    shuffleArray(cards); // Mélanger l'ordre des cartes

    let index = 0;

    const intervalId = setInterval(() => {
      // Change la couleur de la carte actuelle
      changeColor(cards[index]);

      index++;

      // Vérifie si toutes les cartes ont été traitées
      if (index === cards.length) {
        index = 0; // Réinitialise l'indice pour recommencer
        shuffleArray(cards); // Mélanger à nouveau pour la prochaine itération
      }
    }, 800);

    function changeColor(card) {
      const color = randomColorCarte(); // Appel de la fonction pour obtenir une nouvelle couleur
      card.style.backgroundColor = color;
      card.style.transition = "1.2s ease-in-out";
      // Vous pouvez ajouter d'autres animations ou styles si nécessaire
      setTimeout(() => {
        card.style.backgroundColor = ""; // Réinitialise à la couleur par défaut
      }, 900); // Attend 1,2 secondes avant de réinitialiser la couleur
    }
  });
</script>


<div class="carte">
  Site Internet
  <a href="/Sites"><i class="fa-solid fa-desktop banner-icon icon"></i></a>
</div>

<div class="carte">
  Applications
  <a href="/Applications"><i class="fa-solid fa-sitemap icon"></i></a>
</div>

<div class="carte">
  Référencement
  <a href="/Referencement"><i class="fa-solid fa-magnifying-glass-chart banner-icon icon"></i></a>
</div>

<div class="carte">
  Réseaux Sociaux
  <a href="/Marketing"><i class="fa-solid fa-comments-dollar banner-icon icon"></i></a>
</div>

<div class="carte">
  <a href="/Composants"><i class="fa-solid fa-recycle icon"></i></a>
  Composants
</div>

<div class="carte">
  <a href="/Refonte"><i class="fa-solid fa-wand-magic-sparkles banner-icon icon"></i></a>
  Design
</div>

<!-- </div> -->

<style>
  .carte {
    z-index: 0;
    background-color: transparent;
    width: calc(40% - 10px);
    max-width: 300px;
    min-height: 200px;
    display: flex;
    flex-direction: column;
    align-items: center;
    justify-content: center;
    padding: 20px;
    gap: 30px;
    border-radius: 8px;
    box-shadow: 0px 0px 15px rgba(0, 0, 0, 0.514);
    font-family: epilogue;
    color: white;
    font-size: var(--m);
    transition: 0.7s ease-in-out;
    text-transform: capitalize;
    text-align: center;
    border: 1px solid black;
  }
  .carte:hover .icon {
    font-size: 5em;
  }

  .icon {
    transition: 0.7s ease-in-out;
    color: white;
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

  @media screen and (min-width: 801px) and (max-width: 2500px) {
    .carte {
      z-index: 0;
      background-color: transparent;
      width: calc(50% - 10px);
      height: auto;
      display: flex;
      flex-direction: column;
      align-items: center;
      justify-content: center;
      padding: 20px;
    }
  }

  @media screen and (min-width: 300px) and (max-width: 800px) {
    .carte {
      z-index: 0;
      background-color: transparent;
      width: 90%;
      height: auto;
      display: flex;
      flex-direction: column;
      align-items: center;
      justify-content: center;
      padding: 20px;
    }
  }
</style>
