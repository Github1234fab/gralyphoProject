<script>
  // export let icon;
  export let title;
  export let p;
  //   export let number;
  import { fade, slide } from "svelte/transition";
  import arrowUp from "../Assets/png-gralypho/arrowup.svg";
  import arrowDown from "../Assets/png-gralypho/arrowdown.svg";

  let close = false;

  function collapse() {
    close = !close;
  }
</script>

<div class="wrapper {close ? 'active' : ''}">
  <button class="button" on:click={collapse}>
    {title}
    <span class="button-after">
      {#if close}
        <img src={arrowUp} alt="Arrow Up" in:fade={{ duration: 1200 }} />
      {:else}
        <img src={arrowDown} alt="Arrow Down" in:fade={{ duration: 1200 }} />
      {/if}
    </span>
  </button>

  {#if close}
    <span transition:slide={{ duration: 1200 }}>
      <div class="content {close ? 'less' : ''} " in:fade={{ duration: 1200 }} out:fade={{ duration: 1200 }}>
        <p class="p">{p}</p>
      </div>
    </span>
  {/if}
</div>

<style>
  .wrapper {
    display: flex;
    flex-direction: column;
    justify-content: center;
    align-items: center;
    width: 100vw;
  } 
  .button {
    position: relative;
    display: flex;
    padding: 20px;
    color: var(--colorC);
    font-size: 1.3em;
    font-weight: 500;
    cursor: pointer;
    border-top: none;
    border-right: none;
    border-left: none;
    border-bottom: 1px rgb(219, 219, 219) solid;
    background-color: var(--ca);
    width: 80%;
    /* background: linear-gradient(to left, rgb(192, 191, 191), rgb(228, 228, 228)); */
    height: 100px;
    text-align: left;
  }
  .button-after {
    position: absolute;
    content: "{buttonText}";
    color: rgb(100, 100, 229);
    font-size: 1em;
    font-weight: bolder;
    right: 50px;
    align-self: center;
    padding: 20px;
  }
  .button-after img {
    height: 20px;
  }
  .content {
    width: 100%;
    display: flex;
    flex-direction: column;
    align-items: center;
    text-align: center;
    padding: 10px;
    border-radius: 5px;
    margin-bottom: 10px;
    border: none;
  }

  .p {
    font-size: 1.2em;
    font-weight: 300;
    color: var(--bg);
    border: none;
    margin: 0px;
    background-color: rgb(228, 228, 228);
    padding: 20px;
  }

  @media screen and (max-width: 768px) {
    .wrapper {
        display: flex;
    flex-direction: column;
    justify-content: center;
    align-items: center;
    width: 100vw;
    }
    .button{
      font: var(--m);
    }

    .button-after {
      right: 0px;
      margin-top: -30px;
    }
  }
</style>
