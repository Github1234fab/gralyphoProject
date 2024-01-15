<script>
  import burger from "../Assets/png-gralypho/burger-menu-right-svgrepo-com.svg";
  import { fade, slide } from "svelte/transition";

  let toggle = false;
  function display() {
    toggle = !toggle;
    console.log(4);
  }
</script>

<nav class="navigation">
  <h1>GRALYPHO</h1>
  <button class="burger-menu" on:click={display}>
    <img src={burger} alt="" class="burger" class:visible={toggle} />
  </button>

  {#if toggle}
    <span class="span" transition:slide={{ duration: 1200 }}>
      <div in:fade={{ duration: 600 }} out:fade={{ duration: 600 }} class="wrapper-links">
        <a href="/">Home</a>
        <a href="/Sites">Sites Web</a>
        <a href="/Applications">Applications</a>
        <a href="/Referencement">Référencement</a>
        <a href="/Marketing">Marketing</a>
        <a href="/Composants">Composants</a>
        <a href="/Refonte">Refonte</a>
      </div>
    </span>
  {/if}
</nav>

<style>
  .navigation {
    padding: 10px;
    grid-column: 1/13;
    padding: 10px;
    display: grid;
    grid-template-columns: repeat(12, 1fr);
    grid-template-rows: auto;
    height: auto;
    margin-top: 30px;
    margin-left: 0px;
    font-size: 16px;
  }
  .span {
    grid-row: 2;
    grid-column: 2/12;
  }

  h1 {
    grid-column: 1;
    grid-row: 1;
    color: transparent;
    font-family: kanit;
    font-size: 1.5em;
    color: var(--colorC);
    font-weight: 200;
    margin-left: 50px;
  }
  .wrapper-links {
    margin-top: 20px;
    margin-left: 20px;
    display: flex;
    gap: 20px;
    opacity: 1;
  }

  a {
    color: white;
    font-size: 1em;
    font-weight: 300;
    text-decoration: none;
  }

  a:hover {
    color: var(--blue);
  }

  .burger-menu {
    background-color: transparent;
    grid-column: 2;
    grid-row: 1;
    margin-left: 10px;
    width: 50%;
    border: none;
    border-left: 1px grey solid;
    border-top: 1px grey solid;
  }

  .burger {
    height: 30px;
    border: none;
  }
  .burger:hover {
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

  @media screen and (max-width: 768px) {
    .wrapper-links {
      flex-direction: column;
    }
    .navigation{
      font-size: 12px
    }
    a{
      font-size: 1.1em;
    }
  }
</style>
