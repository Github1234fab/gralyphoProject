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
  <div class="wrapper-text-benefices">
  <h1> <div class="title-yellow">Automatisez </div>votre outil digital, 
<div class="title-yellow">Économisez </div>du temps et de l'argent,
<div class="title-yellow">Augmentez</div>votre potentiel client.
  </h1>

  <div class="container-wrapper-benef">
    <div class="wrapper-benef">
      <span>8h</span>
      <!-- <h3>Travaillez tout en dormant!</h3> -->
      <p>
        8 heures, pendant lesquelles vous dormez. <br />8 heures pendant lesquelles votre outil Digital travaille pour
        vous et partout dans le monde !
      </p>
    </div>
    <div class="wrapper-benef2 wrapper-benef">
      <span>50%</span>
      <!-- <h3>Économisez votre temps</h3> -->
      <p>50% de votre temps optimisé grâce à votre site Web ou votre Application.</p>
    </div>
    <div class="wrapper-benef">
      <span>+$<br /> </span>
      <!-- <h3>Gagner de l'argent</h3> -->
      <p>Plus de visibilité, plus de prospects, plus de clients, plus d'argent!</p>
    </div>
  </div>
</section>

<style>
  .section-ben {
    display: grid;
    grid-template-columns: repeat(12, 1fr);
    grid-template-rows: auto;
    gap: 0px;
    background-color: var(--primary);
    /* align-items: center;
    justify-content: center; */
  }
  .wrapper-text-benefices {
    grid-column: 2/12;
    grid-row: 1;
  }
  .title-yellow {
    color: yellow;
    font-size: var(--xl);
    font-weight: 900;
    font-family: epilogue;
    letter-spacing: -1px;
  }
  .section-ben h1 {
    font-size: var(--xl);
    font-weight: 900;
    color: rgb(223, 222, 222);
    font-family: epilogue;
    margin-top: 90px;
  }
  .container-wrapper-benef {
    grid-column: 1/13;
    grid-row: 2;
    display: flex;
    flex-direction: row;
    align-items: baseline;
    justify-content: space-between;
    margin-top: 50px;
    margin-bottom: 40px;
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
    height: 120px;
    width: 120px;
    border-radius: 20%;
    font-family: poppins;
    letter-spacing: -2px;
    font-weight: 600;
    color: transparent;
    font-size: 2.4em;
    -webkit-background-image: linear-gradient(to left, var(--orange) 40%, var(--blue));
    background-image: linear-gradient(to left, var(--orange) 40%, var(--blue));
    -webkit-background-clip: text;
    background-clip: text;
  }
  .wrapper-benef {
    display: flex;
    flex-direction: column;
    width: 100%;
    align-items: flex-start;
    justify-content: flex-start;
    text-align: center;
    margin-top: 20px;
    padding: 10px;
    gap: 40px;
  }
  

  .wrapper-benef p {
    margin-top: 0px;
    font-size: var(--m);
    font-weight: 300;
    color: rgb(210, 210, 210);
    font-family: poppins;
    margin-bottom: 50px;
    text-align: left;
  }

  /* @media only screen and (min-width: 768px) and (max-width: 1100px) {
    .section-ben h1 {
      font-size: var(--xxl);
      font-weight: 900;
      color: var(--colorC);
      font-family: epilogue;
      line-height: 40px;
      margin-top: 90px;
    }
  }
  @media only screen and (min-width: 576px) and (max-width: 768px) {
    .section-ben h1 {
      font-size: var(--xxl);
      font-weight: 900;
      color: var(--colorC);
      font-family: epilogue;
      line-height: 30px;
      margin-top: 90px;
    }
  }
  @media only screen and (min-width: 300px) and (max-width: 576px) {
    .section-ben h1 {
      font-size: var(--xxl);
      font-weight: 900;
      color: var(--colorC);
      font-family: epilogue;
      line-height: 30px;
      margin-top: 90px;
    }
  } */


    @media only screen and (min-width: 300px) and (max-width: 768px) {
.container-wrapper-benef {
  flex-direction: column;
  }
     .wrapper-benef2{
     display: flex;
    flex-direction: column;
    width: 100%;
    align-items: flex-end;
    justify-content: flex-end;
    text-align: center;
    margin-top: 20px;
    padding: 10px;
    gap: 40px;
  }
    .wrapper-benef2 p {
    margin-top: 0px;
    font-size: var(--m);
    font-weight: 300;
    color: rgb(210, 210, 210);
    font-family: poppins;
    margin-bottom: 50px;
    text-align: right;
  }

}
</style>
