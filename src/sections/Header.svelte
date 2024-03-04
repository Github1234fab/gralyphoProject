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
  <div class="wrapper-logo-burger">
  <a href="/" class="logo"><Logo /></a>
  <button class="burger-menu" aria-label="Menu" on:click={display}>
    <i class="fa-solid fa-bars burger" class:visible={toggle}></i>
  </button>
  </div>

  {#if toggle}
    <span class="span" transition:slide={{ duration: 1900 }}>
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

<!-- <div class="hills"></div> -->
<style>
  .navigation {
    width: 100vw;
    display: flex;
    flex-direction: column;
    align-items: center;
    justify-content: center;
    padding: 10px;
    font-size: 16px;
        border-bottom: 1px rgb(74, 74, 74) solid;
  }

  .navigation h1 span {
    color: rgb(218, 216, 216);
    font-weight: 900;
  }
.wrapper-logo-burger{
  display: flex;
  flex-direction: row;
  width: 100%;
  align-items: center;
  justify-content: space-between;
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
  .wrapper-links {
    /* grid-column: span 12;
    grid-row: 2; */
    margin-left: 200px;
    margin-right: 200px;
    display: flex;
    gap: 40px;
    opacity: 1;
    margin-top: 50px;
    margin-bottom: 40px;
    margin-left: 200px;
  }
  a {
    color: white;
    font-size: 1em;
    font-weight: 300;
    text-decoration: none;
    transition: 0.4s ease-in-out;
  }
  a:hover {
    color: grey;
  }
  .burger-menu {
    background-color: transparent;
    border: none;
    grid-column: 6;
    grid-row: 1;
    width: 70px;
    /* border-radius: 4px; */
    /* border: solid 1px grey; */
    padding: 5px;
  
  }
  .burger-menu:hover {
    animation: bounce 0.4s ease-in-out;
  }
  .burger {
    font-size: var(--l);
    border: none;
    color: rgb(218, 216, 216);

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
      /* text-align: left;  */
       gap: 10px;
    }
    .navigation {
      font-size: 16px;
    }
    a {
      font-size: 1.1em;
    }
  }
</style>
