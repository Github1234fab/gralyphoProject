<script>
  export let title;
  export let icon;
  export let p;
</script>

<div class="cards">
  <div class="wrapper-text">
    <img src={icon} alt="" class="icon" />
    <h1>{title}</h1>
    <p>
      {p}
    </p>
  </div>
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
    background: radial-gradient(circle at center, var(--gradient), var(--primary));
    background-size: 130% 100%;
    border: 4px solid var(--bg);
  }
  .icon {
    height: 70px;
    width: 70px;
    padding: 10px;
    color: white;
    border: 1px solid white;
    border-radius: 50%;
  }
  .icon:hover {
    animation: bounce 0.4s ease-in-out;
    border: 2px solid var(--ca);
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
  .wrapper-text h1 {
    font-weight: kanit;
    font-weight: 800;
    font-size: 1.5em;
 text-transform: uppercase;
  }
  .wrapper-text p {
    font-size: 1em;
    color: var(--colorC);
    font-weight: 300;
    text-align: center;
    line-height: 30px;
    padding: 5px;
  }
</style>
