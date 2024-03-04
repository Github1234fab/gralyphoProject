<script>
  import { onMount } from "svelte";
  import EngrenageA from "../Components/EngrenageA.svelte";
  import EngrenageB from "../Components/EngrenageB.svelte";
  import EngrenageC from "../Components/EngrenageC.svelte";
  import { fade } from "svelte/transition";

  function randomColor() {
    const randomComponent = () => Math.floor(Math.random() * 256);
    const color = `rgb(${randomComponent()}, ${randomComponent()}, ${randomComponent()})`;
    return color;
  }

  let transition = "2s ease-in-out";
  let colorA = randomColor();
  let colorB = randomColor();
  let colorC = randomColor();

  function changeColor() {
    colorA = randomColor();
    colorB = randomColor();
    colorC = randomColor();
  }

  onMount(() => {
    setInterval(changeColor, 1800);
  });
</script>

<div class="engrenage-wrapper">
  <div>
    <EngrenageA fill={colorA} {transition} />
  </div>
  <div>
    <EngrenageB fill={colorB} {transition} />
  </div>
  <div>
    <EngrenageC fill={colorC} {transition} />
  </div>
</div>

<style>
  .engrenage-wrapper {
    position: relative;
    width: 100%;
    height: 100%;
  }

  @keyframes rotation {
    0% {
      transform: rotate(0deg);
    }
    100% {
      transform: rotate(360deg);
    }
  }
</style>
