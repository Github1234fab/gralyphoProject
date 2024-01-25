<script>
  export let title;
  export let link;
</script>

<div class="card">
  <h2>{title}</h2>
  <a href={link} target="_blank" class="button linear-gradient">Découvrir</a>
</div>

<style>
  .card {
    flex-shrink: 0;
    border-radius: 8px;
    margin: 8px;
    height: 20em;
    width: 20em;
    user-select: none;
    overflow: hidden;
    display: flex;
    flex-direction: column;
    justify-content: center;
    align-items: center;
    padding: 10px;
    border: 1px solid rgb(105, 105, 105);
    box-shadow: 3px 3px 5px rgba(0, 0, 0, 0.336);
    background-color: var(--bg);
  }
  /* .linear-gradient{
    border-style: solid;
    border-width: 3px;
    border-image: linear-gradient(45deg, rgb(143, 55, 0), rgb(66, 228, 250)) 1;
  } */
  .button {
    padding: 30px;
    border-radius: 10px;
    width: auto;
    height: auto;
    color: var(--orange);
    text-decoration: none;
    margin-bottom: 30px;
    margin-top: 20px;
    font-weight: 300;
    font-size: 1.2em;
    transition: 0.4s ease-in-out;
    background-color: var(--bg);
    border: 1px solid rgb(167, 167, 167);
    font-family: kanit;
  }
  .button:hover {
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
  .card h2 {
    z-index: 1;
    font-family: epilogue;
    font-weight: 300;
    font-size: var(--l);
    color: var(--colorC);
    padding: 10px;
    text-align: center;
  }
  /* .card h2 span {
    font-weight: 900;
    color: transparent;
    -webkit-background-image: linear-gradient(to left, var(--ca), var(--blue));
    background-image: linear-gradient(to left, var(--ca), var(--blue));
    -webkit-background-clip: text;
    background-clip: text;
  } */
</style>
