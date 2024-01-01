<script>
  // export let icon;
  export let title;
  export let p;
  //   export let number;
  import { fade, slide } from "svelte/transition";

  let close = false;
  let buttonText = "+";

  function collapse() {
    close = !close;
    buttonText = close ? "-" : "+";
  }
</script>

<div class="wrapper {close ? 'active' : ''}">
  <div class="button" on:click={collapse}>{title} <span class="button-after" in:fade out:fade>{buttonText}</span></div>

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
    width: 100%;
  }
  .button {
    position: relative;
    display: flex;
    background-color: var(--colorO);
    padding: 18px;
    border-radius: 5px;
    color: white;
    font-size: 1.2em;
    font-weight: 500;
    cursor: pointer;
    margin-bottom: 10px;
    box-shadow: 3px 3px 15px rgb(1, 6, 27);
  }
  .button-after {
    position: absolute;
    content: "{buttonText}";
    color: rgb(100, 100, 229);
    font-size: 2em;
    font-weight: bolder;
    right: 30px;
    align-self: center;
  }
  .content {
    width: 100%;
    display: flex;
    flex-direction: column;
    padding: 10px;
    border-radius: 5px;
    margin-bottom: 10px;
    border: none;
  }

  .p {
    font-size: 1.2em;
    font-weight: 300;
    color: white;
    border: none;
  }
</style>
