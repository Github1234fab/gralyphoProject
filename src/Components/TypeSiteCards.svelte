<script>
  export let title;
  export let icon;
  export let p;
  export let lien;
</script>

<div class="cards">
  <div class="wrapper-text">
    <img src={icon} alt="icon de types de sites" class="icon" />
    <h1>{title}</h1>
    <p>
      {p}
    </p>
  </div>
  <button class="button" href={lien}>En savoir plus<button /> </button>
</div>

<style>
  .cards {
    display: flex;
    flex-direction: column;
    width: calc(30% - 10px);
    height: calc(50% - 10px);
    border-radius: 20px;
    box-shadow: 0px 0px 10px 0px rgba(0, 0, 0, 0.28);
    color: white;
    justify-content: center;
    align-items: center;
    /* background: radial-gradient(circle at center, var(--gradient), var(--primary));
    background-size: 130% 100%; */
    background-color: var(--primary);
    border: 2px solid var(--bg);
  }
  .icon {
    height: 60px;
    width: 60px;
    padding: 10px;
    color: blue;
    border: 1px solid white;
    border-radius: 50%;
    text-align: center;
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
  .button {
    background-color: transparent;
    border: 2px solid #7f00fd;
    border-radius: 10px;
    padding: 10px;
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
  .wrapper-text h1 {
    font-weight: kanit;
    font-weight: 800;
    font-size: 1.5em;
    /* text-transform: uppercase; */
  }
  .wrapper-text p {
    font-size: 1em;
    color: var(--colorC);
    font-weight: 300;
    text-align: center;
    line-height: 30px;
    padding: 5px;
  }

  @media screen and (max-width: 768px) {
    .cards {
      width: calc(100% - 10px);
      height: auto;
    }
  }
</style>
