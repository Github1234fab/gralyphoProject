<script>
  export let title;
  export let icon;
  export let p;
  export let lien;
</script>

<div class="cards">
  <div class="wrapper-text">
    <a href={lien}><img src={icon} alt="icon de types de sites" class="icon" /></a>
    <h1>{title}</h1>
    <p>
      {p}
    </p>
  </div>
  <!-- <a href={lien}><button class="button">En savoir plus<button /></button></a> -->
</div>

<style>
  .cards {
    display: flex;
    flex-direction: column;
    border-radius: 8px;
    box-shadow: 0px 0px 10px 0px rgba(0, 0, 0, 0.28);
    color: white;
    justify-content: center;
    align-items: center;
    background-color: var(--orange);
    border: 1px solid #D1A617;
    width: calc(30% - 10px);
    height: calc(50% - 10px);
  }
  .icon {
    height: 100px;
    width: 100px;
    padding: 10px;

  }
  .icon:hover{
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
  /* .button {
    background-color: var(--blue);
    border: none;
    border-radius: 8px;
    padding: 14px;
    color: white;
    font-family: Kanit;
    font-size: 1em;
    font-weight: 400;
    transition: 0.4s ease-in-out;
    text-align: center;
    width: 150px;
    margin-bottom: 50px;
  }
  .button:hover {
    animation: bounce 0.4s ease-in-out;
  } */

  .wrapper-text {
    display: flex;
    flex-direction: column;
    gap: 50px;
    align-items: center;
    width: 100%;
    height: 100%;
    padding: 30px;
  }
  .wrapper-text h1 {
    font-weight: kanit;
    font-weight: 800;
    font-size: var(--xl);
    /* text-transform: uppercase; */
  }
  .wrapper-text p {
    font-size: var(--l);
    color: var(--colorC);
    font-weight: 300;
    text-align: center;
    line-height: 30px;
    padding: 5px;
  }

  @media screen and (max-width: 1116px) {
    .cards {
      width: calc(40% - 10px);
      height: calc(37% - 10px);
    }
  }

  @media screen and (max-width: 768px) {
    .cards {
      width: calc(100% - 10px);
      height: auto;
    }
  }
</style>
