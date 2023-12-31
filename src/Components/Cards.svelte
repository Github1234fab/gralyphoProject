<script>
  export let title;
  export let link;
</script>

<div class="card">
  <h2>{title}</h2>
  <a href={link} target="_blank"><button class="button">Voir</button></a>
</div>

<style>
  .card {
    /* position: relative; */
    flex-shrink: 0;
    border-radius: 3px;
    border: none;
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
    box-shadow: 3px 3px 15px rgb(1, 6, 27);
    background-color: #152a37;
  }
  .button {
    background-color: rgb(100, 100, 229);
    padding: 30px;
    border-radius: 10px;
    width: auto;
    height: auto;
    color: white;
    text-decoration: none;
    margin-bottom: 30px;
    margin-top: 20px;
    font-weight: 400;
    font-size: 1em;
    transition: 0.4s ease-in-out;
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
    word-wrap: break-word;
    z-index: 1;
    font-family: kanit;
    font-weight: 500;
    font-size: 1.3em;
    color: white;
    padding: 10px;
    text-align: center;
  }
</style>
