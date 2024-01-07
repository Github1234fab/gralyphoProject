<script>
  import "./styles.css";
  import Footer from "../sections/Footer.svelte";
  import burger from "../Assets/png-gralypho/burger-menu-right-svgrepo-com.svg";
  import { fade, slide } from "svelte/transition";
  // import Header from "../sections/Header.svelte";

  let toggle = false;
  function display() {
    toggle = !toggle;
    console.log(4);
  }
</script>

<main>
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
  <!-- <Header/> -->
  <slot />
  <Footer />
</main>

<style>
  main {
    /* background-color: var(--colorO); */
    overflow: hidden;
 
  }

  h1 {
    grid-column: 2;
    grid-row: 1;
    color: var(--colorN);
    font-family: kanit;
    font-size: 1.5em;
    margin-left: 45px;
  }

  .navigation {
    margin-top: 30px;
    background-color: var(--colorO);
    display: grid;
    grid-template-columns: repeat(12, 1fr);
    grid-template-rows: auto;
    height: auto;
  }
  .span {
    grid-row: 2;
    grid-column: 2/12;
  }

  .wrapper-links {
    margin-top: 20px;
    margin-left: 20px;
    display: flex;
    gap: 20px;
    opacity: 1; /* Initial opacity */
  }

  a {
    color: white;
    font-size: 0.7em;
    font-weight: 200;
    text-decoration: none;
  }

  a:hover {
    color: var(--colorD);
  }

  .burger-menu {
    background-color: transparent;
    grid-column: 3;
    grid-row: 1;
    margin-left: 20px;
    width: 50%;
  }

  .burger {
    height: 30px;
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

  @media screen and (max-width: 768px){
    .wrapper-links{
      flex-direction: column;
    }
  }
</style>
