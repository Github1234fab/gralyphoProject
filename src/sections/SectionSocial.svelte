<script>
  import Social from "../Components/Social.svelte";
  let socialTab = [
//     {
//       title: "Travail en Ligne et Collaboration :",
//       p: "Nous avons adopté le pouvoir de la dématérialisation pour transcender les frontières géographiques. Notre équipe travaille de manière virtuelle, utilisant des outils en ligne de pointe pour garantir une communication fluide, une coordination efficace et des résultats exceptionnels.",
//     },
    {
      title: "Flexibilité Globale",
      p: "Avec notre modèle dématérialisé, nous avons accès à un réseau mondial de talents. Cela signifie que votre projet est entre les mains des meilleurs experts, indépendamment de leur emplacement géographique.",
    },
    {
      title: "Optimisation Budgétaire",
      p: "La dématérialisation nous permet de minimiser les coûts fixes associés aux locaux physiques. Nous investissons davantage dans la qualité de votre projet, assurant une efficacité opérationnelle maximale tout en optimisant votre budget.",
    },
    {
      title: "Durabilité Environnementale",
      p: "En adoptant la dématérialisation, nous contribuons à la durabilité environnementale en réduisant notre empreinte écologique. C'est une approche moderne qui aligne la réussite de votre projet avec une conscience écologique.",
    },
  ];
</script>

<section class="section">
        <div class="wrapper-text">
  <h1>Agence <br> <span> Ecoresponsable.</span></h1>
 <div class="wrapper-trees">
         <i class="fa-solid fa-tree-city tree-icon"></i>
  <i class="fa-solid fa-tree tree-icon"></i>
  <i class="fa-brands fa-pagelines tree-icon"></i>
 </div>
  </div>
 
  <div class="wrapper-social">
    {#each socialTab as social}
      <Social title={social.title} p={social.p} />
    {/each}
  </div>
</section>

<style>
  .section {
    display: flex;
    flex-direction: column;
    width: 100%;
    gap: 30px;
    background-color: var(--colorC);

  }
  .wrapper-text{
        display: flex;
        flex-direction: column;
        width: 100%;
        align-items: center;
        justify-content: center;
        text-align: center;
        margin-top: 20px;
 
  }
  .wrapper-social {
    display: flex;
    width: 100%;
  }
  .wrapper-trees{
        display: flex;
        width: 100%;
        justify-content: center;
        align-items: center;
        gap: 20px;
        margin-top: 20px;
  }
  .tree-icon{
        font-size: 50px;
        color: var(--primary);
        text-shadow: 2px 3px 10px rgba(0, 49, 0, 0.425);       
  }
  .section h1 {
    font-size: var(--xl);
    font-weight: 900;
    color: var(--primary);
    margin-top: 10px;
    margin-bottom: 10px;
    font-family: epilogue;
  }
.section h1 span {
    font-weight: 900;
    color: transparent;
    -webkit-background-image: linear-gradient(to left, green, var(--blue));
    background-image: linear-gradient(to left, green, var(--blue));
    -webkit-background-clip: text;
    background-clip: text;
  }

  /* .section h2 {
    font-size: var(--l);
    font-weight: 800;
    color: var(--primary);
    margin-top: 10px;
    margin-bottom: 10px;
    font-family: epilogue;
  } */

    @media screen and (max-width: 768px){
        .wrapper-social{
         flex-direction: column;
        }
  }
</style>
