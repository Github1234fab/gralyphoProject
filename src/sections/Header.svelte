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
  <a href="/" class="logo"><Logo /></a>
  <button class="burger-menu" aria-label="Menu" on:click={display}>
    <i class="fa-solid fa-bars burger" class:visible={toggle}></i>
  </button>

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
  /* .navigation h1 {
    grid-column: 2/11;
    margin-left: 200px;
    margin-right: 200px;
    grid-row: 1;
    font-size: var(--m);
    color: rgb(218, 216, 216);
    font-weight: 200;
    text-align: center;

  } */
  .navigation h1 span {
    color: rgb(218, 216, 216);
    font-weight: 900;
  }
  /* .hills  {
    margin-top: -20px;
    width: 100vw;
    height: 100px;
   border-bottom: white 1px solid;
    background-color: #1f2228;
     /* background-image: linear-gradient(to top, rgb(66, 130, 64) , var(--orange) 30%);  */
  /* clip-path: polygon(198px 45px, 274px 49px, 339px 23px, 354px 23px, 365px 23px, 462px 53px, 485px 49px, 529px 72px, 590px 50px, 672px 65px, 737px 53px, 779px 55px, 868px 49px, 885px 55px, 952px 41px, 1052px 55px, 1079px 55px, 1164px 72px, 1263px 55px, 1383px 41px, 1421px 28px, 1455px 23px, 1491px 23px, 1538px 15px, 1573px 4px, 1608px 0px, 1670px 23px, 1732px 49px, 1786px 65px, 1872px 55px, 1924px 82px, 2000px 100px, 0px 100px, 129px 72px) */
  /* }  */
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
    font-size: 3.6em;
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
       gap: 10px;
    }
    .navigation {
      font-size: 12px;
    }
    a {
      font-size: 1.1em;
    }
  }
</style>
