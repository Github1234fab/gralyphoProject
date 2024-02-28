<script>
  import { onMount } from "svelte";

  onMount(() => {
    gsap.to(".section-ben", {
      opacity: 1,
      ease: "expoScale",
      scrollTrigger: {
        trigger: ".section-ben",
        start: "top 950px",
        end: "100px",
        scrub: 3,
      },
    });
  });
</script>

<section class="section-ben">
  <h1>
    <div class="automatisez">Automatisez</div>
    <br />
    <div class="economisez">Économisez</div>
    <br />
    <div class="augmentez">Augmentez</div>
  </h1>
  <div class="container-wrapper-benef">
    <div class="wrapper-benef">
      <span>8h</span>
      <h3>Travaillez tout en dormant!</h3>
      <p>
        8 heures, pendant lesquelles vous dormez. <br />8 heures pendant lesquelles votre outil Digital travaille pour
        vous et partout dans le monde !
      </p>
    </div>
    <div class="wrapper-benef">
      <span>50%</span>
      <h3>Économisez votre temps</h3>
      <p>50% de votre temps optimisé grâce à votre site Web ou votre Application.</p>
    </div>
    <div class="wrapper-benef">
      <span>$<br /> </span>
      <h3>Gagner de l'argent</h3>
      <p>Plus de visibilité, plus de prospects, plus de clients, plus d'argent!</p>
    </div>
  </div>
</section>

<style>
  .section-ben {
    display: flex;
    flex-direction: column;
    width: 100%;
    gap: 0px;
    background-color: var(--primary);
    align-items: center;
    justify-content: center;
    text-align: center;
    opacity: 0.2;
  }
  .automatisez {
    color: rgb(179, 177, 177);
  }
  .augmentez {
    color: rgb(255, 255, 255);
  }
  .economisez {
    color: rgb(225, 224, 224);
  }
  .section-ben h1 {
    font-size: var(--xxl);
    font-weight: 900;
    color: var(--colorC);
    font-family: epilogue;
    line-height: 60px;
    margin-top: 90px;
  }
  .container-wrapper-benef {
    margin-top: 70px;
    margin-bottom: 70px;
    gap: 40px;
  }
  .section-ben span {
    justify-content: center;
    align-items: center;
    display: flex;
    text-align: center;
    border: 1px solid rgb(95, 95, 95);
    box-shadow:
      2px 3px 5px 4px rgba(0, 0, 0, 0.467) inset,
      -2px -3px 5px 4px rgba(0, 0, 0, 0.489) inset;
    height: 160px;
    width: 160px;
    border-radius: 20%;
    font-family: poppins;
    letter-spacing: -2px;
    font-weight: 600;
    color: transparent;
    font-size: 3em;
    -webkit-background-image: linear-gradient(to left, var(--orange) 40%, var(--blue));
    background-image: linear-gradient(to left, var(--orange) 40%, var(--blue));
    -webkit-background-clip: text;
    background-clip: text;
  }
  .wrapper-benef {
    display: flex;
    flex-direction: column;
    width: 100%;
    align-items: center;
    justify-content: center;
    text-align: center;
    margin-top: 20px;
    padding: 10px;
    gap: 40px;
  }
  .wrapper-benef h3 {
    font-size: var(--l);
    font-weight: 700;
    color: rgb(172, 172, 172);
    font-family: epilogue;
  }
  .wrapper-benef p {
    margin-top: -20px;
    font-size: var(--m);
    font-weight: 300;
    color: var(--colorC);
    font-family: epilogue;
    margin-bottom: 50px;
  }
</style>
