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
  <!-- <h1 class="title">GRALYPHO</h1> -->
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
    padding: 10px;
    margin-top: 30px;
    font-size: 16px;
  }
  .title-link {
    grid-column: 2;
    grid-row: 1;
    margin-left: 20px;
  }
  .span {
    grid-row: 3;
    grid-column: 4/12;
  }
  .wrapper-links {
    display: flex;
    gap: 40px;
    opacity: 1;
    margin-top: 20px;
  }
  a {
    color: white;
    font-size: 1em;
    font-weight: 300;
    text-decoration: none;
  }
   a:hover {
    color:  #7f00fd;
  }
  .burger-menu {
    background-color: transparent;
    border: none;
    grid-column: 3;
    grid-row: 1;

    width: 50px;
    border-radius: 8px;
  }
   .burger-menu:hover {
    animation: bounce 0.4s ease-in-out;
  }
  .burger {
    height: 40px;
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
