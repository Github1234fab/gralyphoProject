<script>
  import burger from "../Assets/png-gralypho/burger-menu-right-svgrepo-com.svg";
  import { fade, slide } from "svelte/transition";
  import Logo from "../Components/Gralypho.svelte";
    import Engrenage from "../Components/Engrenages.svelte";

  let toggle = false;
  function display() {
    toggle = !toggle;
    console.log(4);
  }
</script>

<nav class="navigation">
  <div class="wrapper-logo-burger">
   
    <a href="/" class="logo"> <Engrenage/></a>
    <!-- <Logo /> -->
    <h1 class="title">Gralypho, créateur de site Web & Application</h1>
    <button class="burger-menu" aria-label="Menu" on:click={display}>
      <i class="fa-solid fa-bars burger" class:visible={toggle}></i>
    </button>
  </div>

  {#if toggle}
    <span class="span" transition:slide={{ duration: 1900 }}>
      <div in:fade={{ duration: 600 }} out:fade={{ duration: 600 }} class="wrapper-links">
        <!-- <a href="/">Home</a> -->
        <a class="link-contact" href="/Sites">Sites Web</a>
        <a class="link-contact" href="/Applications">Applications</a>
        <a class="link-contact" href="/Referencement">Référencement</a>
        <a class="link-contact" href="/Marketing">Media Sociaux</a>
        <a class="link-contact" href="/Refonte">Design</a>
        <a class="link-contact" href="/Composants">Stratégie</a>
      </div>
    </span>
  {/if}
</nav>

<!-- <div class="hills"></div> -->
<style>
  .navigation {
    grid-template-columns: repeat(12, 1fr);
    grid-template-rows: auto;
    width: 100vw;
    display: flex;
    flex-direction: column;
    align-items: center;
    justify-content: center;
    padding: 30px;
    font-size: 16px;
    /* border-bottom: 1px rgb(74, 74, 74) solid; */
    background-color: var(--primary);
    z-index: 2;
  }

  .navigation h1 span {
    color: rgb(218, 216, 216);
    font-weight: 900;
  }
  .wrapper-logo-burger {
    grid-column: 1/13;
    grid-row: 1;
    display: flex;
    flex-direction: row;
    width: 100%;
    align-items: baseline;
    justify-content: space-between;
    z-index: 3;
  }
  .logo {
    grid-column: 5;
    grid-row: 1;
    display: flex;
    flex-direction: column;
    justify-content: center;
    align-items: center;
    margin-top: 10px;
    margin-bottom: 5px;
  }
  .span {
    grid-row: 3;
    grid-column: 2/12;
  }
  .title {
    font-family: poppins;
    font-size: 0.8em;
    font-weight: 300;
    color: rgb(209, 205, 205);
  }

  .wrapper-links {
    grid-column: 1/13;
    grid-row: 2;
    display: flex;
    align-items: center;
    justify-content: center;
    gap: 26px;
    opacity: 1;
    margin-top: 50px;
    margin-bottom: 40px;
    width: 100vw;
    z-index: 2;
  }
  a {
    color: white;
    font-size: 1em;
    font-weight: 300;
    text-decoration: none;
    transition: 0.4s ease-in-out;
      z-index: 2;
  }
  a:hover {
    transition: 0.4s ease-in-out;
    color: grey;
  }
  .burger-menu {
    background-color: transparent;
    border: none;
    grid-column: 6;
    grid-row: 1;
    width: 70px;
    padding: 5px;
  }
  .burger-menu:hover {
    animation: bounce 0.4s ease-in-out;
  }
  .burger {
    font-size: var(--l);
    border: none;
    color: var(--CTA);
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
      justify-content: center;
      align-items: center;
      gap: 10px;
    }
    .title {
      width: 0px;
      display: none;
    }
    .navigation {
      font-size: 16px;
    }
    .link-contact {
      font-size: 1.1em;
    }
    .burger-menu {
      z-index: 2;
    }
  }
</style>
