<script>
  import burger from "../Assets/png-gralypho/burger-menu-right-svgrepo-com.svg";
  import { fade, slide } from "svelte/transition";
  import Logo from "../Components/Gralypho.svelte";

  let toggle = false;
  function display() {
    toggle = !toggle;
    console.log(4);
  }
</script>

<nav class="navigation">
  <a href="/" class="title-link"><Logo/></a>
  <button class="burger-menu" on:click={display}>
    <img src={burger} alt="" class="burger" class:visible={toggle} />
  </button>

  {#if toggle}
    <span class="span" transition:slide={{ duration: 1200 }}>
      <div in:fade={{ duration: 600 }} out:fade={{ duration: 600 }} class="wrapper-links">
        <!-- <a href="/">Home</a> -->
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
    width: 100vw;
    display: grid;
    grid-template-columns: repeat(12, 1fr);
    grid-template-rows: repeat(3, auto);
    padding: 20px;
    font-size: 16px;
        background-color: var(--bg);

  }
  .title-link {
    grid-column: 2;
    grid-row: 1;
    margin-left: -5px;
  }
  .span {
    grid-row: 3;
    grid-column: 2/12;
  }
  .wrapper-links {
    display: flex;
    gap: 40px;
    opacity: 1;
    margin-top: 40px;
    margin-bottom: 40px;
  }
  a {
    color: white;
    font-size: 1em;
    font-weight: 300;
    text-decoration: none;
    transition: 0.3s ease-in-out;
  }
   a:hover {
color: grey;
  }
  .burger-menu {
    background-color: transparent;
    border: none;
    grid-column: 3;
    grid-row: 1;
    width: 50px;
    border-radius: 8px;
    margin-top: 0px;
  }
   .burger-menu:hover {
    animation: bounce 0.4s ease-in-out;
  }
  .burger {
    height: 45px;
    border: none;
    padding: 5px;
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
    .navigation {
      font-size: 12px;
    }
    a {
      font-size: 1.1em;
    }
  }
</style>
