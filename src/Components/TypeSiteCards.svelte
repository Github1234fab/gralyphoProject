<script>
  export let title;
  export let icon;
  export let p;
  export let lien;
  export let lien2;
</script>

<div class="cards">
  <div class="wrapper-text">
    <a href={lien}><img src={icon} alt="icon de types de sites" class="icon" /></a>
    <a href={lien2} class="title">{title}</a>
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
    background-color: var(--ca);
    border: 1px solid grey;
    width: calc(30% - 10px);
    height: calc(50% - 10px);
  }
  .icon {
    height: 100px;
    width: 100px;
    padding: 10px;
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

  .wrapper-text {
    display: flex;
    flex-direction: column;
    gap: 50px;
    align-items: center;
    width: 100%;
    height: 100%;
    padding: 30px;
  }
  .title {
    font-weight: kanit;
    font-weight: 900;
    font-size: var(--l);
    border: 1px solid grey;
    padding: 20px;
    border-radius: 8px;
    text-decoration: none;
    color: var(--colorC);
  }
  .title:hover {
    animation: bounce 0.4s ease-in-out;
  }
  .wrapper-text p {
    font-size: 1.3em;
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
