<script>
  import ListValue from "../Components/ListValue.svelte";

  let values = [
    {
      icon: "🚀",
      title: "Innovation Guidée par la Stratégie : ",
      p: " Nous apportons une approche stratégique à chaque aspect de votre présence digitale, de la conception web à la stratégie marketing, en vous aidant à atteindre vos objectifs commerciaux. Nous vous aidons à définir votre stratégie digitale et à la mettre en œuvre pour obtenir des résultats tangibles.",
    },
    {
      icon: "💡",
      title: "Solutions Personnalisées : ",
      p: "Chaque entreprise est unique. Nous développons des solutions digitales sur mesure qui s'adaptent à vos besoins spécifiques, vous permettant de vous démarquer dans un monde en constante évolution. Design, Ux, Ui, contenu textuels (...), rien n'est laissé au hasard pour que vous puissiez réussir sur le Web.",
    },
    {
      icon: "🌐",
      title: "Expansion Digitale : ",
      p: "Explorez de nouveaux horizons grâce à notre expertise en expansion digitale. Que vous soyez une start-up ambitieuse ou une entreprise établie, nous vous aidons à conquérir des marchés en ligne et à maximiser votre impact.",
    },
    {
      icon: "🤝",
      title: "Partenariat axé sur la collaboration : ",
      p: " Nous croyons en la co-création. En travaillant en étroite collaboration avec votre équipe, nous faisons de votre vision une réalité, offrant une expérience transparente et collaborative à chaque étape du processus.",
    },
    {
      icon: "🔐 ",
      title: "Sécurité et Fiabilité : ",
      p: "La sécurité de vos données et la fiabilité de vos systèmes sont notre priorité. Nous adoptons les normes les plus strictes pour assurer la protection de votre entreprise dans l'univers digital.",
    },
  ];
</script>

<section class="section-value">
  <h1>Réinventez aujourd'hui pour exceller demain.</h1>
  <div class="wrapper-list">
    {#each values as value}
      <ListValue icon={value.icon} p={value.p} title={value.title} />
    {/each}
  </div>
</section>

<style>
  .section-value {
    display: flex;
    flex-direction: column;
    height: auto;
    font-size: 16px;
    z-index: 1;
    background-color: white;
    background-position: center;
    padding: 30px;
    gap: 0px;
  }
  .section-value h1 {
    font-family: epilogue;
    font-weight: 900;
    font-size: 2.8em;
    color: var(--primary);
    text-align: left;
    margin: 50px;
  }

  .wrapper-list {
    display: flex;
    flex-direction: column;
    margin: 20px;
    width: 100%;
    margin-bottom: 50px;
  }
  @media screen and (max-width: 768px) {
    .section-value {
      font-size: 12px;
    }
  }
</style>
