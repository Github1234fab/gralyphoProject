<script>
  // export let icon;
  export let title;
  export let p;
  //   export let number;
  	import { fade } from 'svelte/transition';
		import { slide } from 'svelte/transition';

let close= false;

  function collapse() {
    close = !close;
  }
</script>

<div class="wrapper {close ? 'active' : ''}">
  <div class="button" on:click={collapse}>{title}</div>
 {#if  close}
    <div class="content" transition:slide={{ duration: 900}}  transition:fade={ opacity: 1}}>
      <p class="p">{p}</p>
    </div>
  {/if}
</div>

<style>
  .wrapper {
    display: flex;
    flex-direction: column;
    width: 100%;
  }
  .button {
    display: flex;
    
    background-color: var(--colorO);
    padding:18px;
    border-radius: 5px;
    color: white;
    font-size: 1.2em;
    font-weight: 500;
    cursor: pointer;
    margin-bottom: 10px;
    box-shadow:
      3px 5px 6px black,
      -3px -5px 6px black;
  }
  .content {
    width: 100%;
    display: flex;
    flex-direction: column;
    padding: 10px;
    border-radius: 5px;
    margin-bottom: 10px;
    box-shadow: 3px 5px 6px black;
    opacity: 0.5;
  }

  .p {
    font-size: 1.2em;
    font-weight: 300;
      color: white;
  }
 

</style>
