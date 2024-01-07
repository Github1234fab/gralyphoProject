<script>
  import Robot from "../Assets/png-gralypho/Saly-39.png";
  import { onMount } from "svelte";
  import triangle from "../Assets/png-gralypho/nnneon (6).svg";

  onMount(() => {
    gsap.to(".gsap", {
      scale: 1,
      ease: "expoScale",
      scrollTrigger: {
        trigger: ".gsap",
        start: "top 700px",
        end: "-200px",
        scrub: 1,
      },
    });
  });
</script>

<section class="C-section" id="sectionC">
  <div class="wrapper-text">
    <img src={Robot} alt="icon de robot en 3D" class="robot gsap" />
    <img src={triangle} alt="icon de robot en 3D" class="triangle gsap" />
    <h1>La technologie à votre service!</h1>
  
    <p>
      <span>Plateforme et développement</span> <br><br>
      Pour le développement de votre site internet ou votre application, nous avons le choix entre de nombreuses
      technologies! Par technologies nous entendons les plateformes avec lesquelles nous pourrons créer, mais aussi
      déployer et héberger votre outil digital.  <br><br> 
      Vous avez sûrement entendu parler de Wordpress? de Wix? ou encore
      Shopify? Woo Commerce? Squarespace ? Webflow? (...) .  Toutes ces plateformes nous permettent de créer votre outil digital en utilisant très peu de code, ou pas du tout et en bénéficant du CMS associé à ses plateformes<br />
      Mais, nous pouvons tout aussi bien développer votre site internet ou votre application en utilisant exclusivement du code informatique (html/css/Js) et en passant par un Framework, celui que nous utilisons est le bien nommé SVELTE. <br /> <br>
          <span>Choisir la technologie la plus approprié au projet c'est se donner toutes les chances de réussir!</span> <br><br>
      Alors quelle technologie choisir pour obtenir le meilleur de votre outil digital afin que vous puissiez atteindre
      les objectifs que vous vous êtes fixés?<br>
       Et bien, et ce n'est pas une réponse de Normand, mais la réponse est : "Cela dépend de votre projet". Car en effet, chaque projet d'application et chaque site internet qu'il soit un Site vitrine, un Site e-commerce, un Blog, un Portfolio, un Site institutionnel, un Forum, un Réseau social, une Landing page, un Site d'actualités ou encore un Site éducatif requiert en matière de conception, de réalisation et de déploiement des besoins très différents et variables. <br><br>
       
       <span>Wordpress et CMS ou programmation?</span> <br><br>
       Wordpress est bien oui, mais pas pour tout et présente des avantages et des inconvénients. Il peut être rapide pour la conception avec son système de Drag and Drop et ses templates, mais si un template n'est plus mis à jour par son concepteur, vous perdez votre site.  <br> Wordpress est peu cher, mais les budgets pour étendre ses fonctionnalités peuvent atteindre des coûts impressionnants. <br> Wordpress peut être simple avec ses plugins, mais les plugins peuvent considérablement réduire les temps de chargements. Et pour chaque plateforme et méthode de développement ce sera pareil. Elles possèderont toutes des avantages et des inconvénients. <br><br>
<span>Technologie appropriée = budget maîtrisé =  délai respecté.</span> <br><br>
   Faire le choix de la bonne méthode et de la meilleure palteforme, bien  en amont de la réalisation de votre application ou de votre site Web sera déterminant pour la réalisation de votre outil digital. Ce choix sera totalement imbriqué avec le budget final de votre outil digital. Nous le savons tous, le temps, c'est de l'argent. Alors nous devons faire le bon choix pour optimiser au maximum le temps de travail et le résultat final de votre outil digital , ainsi que son budget et ses capacités futures. </p>
  </div>
</section>

<style>
  .C-section {
    display: grid;
    grid-template-columns: repeat(12, 1fr);
    grid-template-rows: 1;
    height: auto;
    font-size: 16px;
        background: radial-gradient(circle at top, var(--colorN), var(--colorO));
    background-size: 100% 100%;
    shape-outside: circle(90%);
    margin-top: 0px;

  }
  .wrapper-text {

        /* background: radial-gradient(circle, var(--colorO), var(--colorN)); */
    grid-column: 2/12;
    grid-row: 1;
    display: grid;
    grid-template-columns: repeat(12, 1fr);
    grid-template-rows: 1;
    border-radius: 20px;
    padding: 20px;
    display: flex;
    flex-direction: column;
    /* border: solid 1px rgb(55, 55, 55); */
  }
  .C-section h1 {
    word-wrap: break-word;
    grid-column: 2/12;
    grid-row: 1;
    text-align: left;
    font-family: epilogue;
    font-weight: 800;
    font-size: 1.7em;
    color: white;
    margin-top: 50px;
    padding: 10px;
    line-height: 37px;
  }

  .C-section p {
         column-count: 4; /* ou le nombre de colonnes souhaité */
  column-gap: 20px;
    grid-column: 2/12;
    grid-row: 3;
    color: var(--colorC);
    margin-top: 20px;
    text-align: left;
    line-height: 30px;
    font-weight: 300;
    font-size: 1.1em;
    font-family: epilogue;
    padding: 10px;
  }
  .C-section p span{
    font-weight: 700;
  }
  .robot {
    transform: scale(0.6);
    height: 180px;
    width: 180px;
    margin-top: 50px;
    z-index: 2;
    align-self: center;
  }
  .triangle {
    transform: scale(0.2);
    height: 180px;
    margin-top: -180px;
    z-index: 1;
    align-self: center;
  }
  .gsap {
    opacity: 1;
  }

  @media screen and (max-width: 768px) {
    .C-section {
      font-size: 13px;
    }
    .wrapper-text{
      background-size: 100%;
    }
  }
</style>
