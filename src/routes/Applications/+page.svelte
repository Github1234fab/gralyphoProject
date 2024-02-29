<script>
  import { fade, slide } from "svelte/transition";
  // import bg from "../../Assets/png-gralypho/41.png";
  import Header from "../../sections/Header.svelte";
</script>

<Header />
<section class="" in:fade={{ duration: 3000 }}>
  <div class="wrapper background-animated">
    <h1>Développement d'Application</h1>
    <!-- <img src={bg} alt="" class="bg" /> -->
    <p>
      "Propulsez votre entreprise vers l'avenir avec nos services de conception et de développement d'applications sur
      mesure. Chez Gralypho, nous créons des solutions innovantes qui répondent parfaitement à vos besoins. De la
      planification initiale à la mise en œuvre et au-delà, notre équipe d'experts assure un processus transparent et
      efficace. Découvrez comment nous pouvons transformer vos idées en applications exceptionnelles, prêtes à conquérir
      le marché."<br /><br />
    </p>
    <p>
      <span>Quelle est la durée estimée pour le développement d'une application' ?</span> <br /><br />
      <li>
        La durée de développement d'une application dépend de la complexité de votre projet. <br />
        S'il s'agit d'une application simple, le délai peut varier entre 1 et deux mois. Au-delà, il s'agit d'application
        plus complexes, le délai peut varier entre 3 et 6 mois.
      </li>
      <br /><br />
    </p>

    <h4>
      Pour le développement d'application, il est essentiel que nous puissions nous rencontrez. <br />Alors parlez nous
      de votre projet, autour d'un café!
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
  .wrapper li {
    z-index: 2;
    color: var(--colorC);
  }
</style>
