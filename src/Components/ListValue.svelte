<script>
  export let icon;
  export let p;
  export let title;
  import { onMount } from "svelte";

  onMount(() => {
    gsap.to(".icon", {
      x: 0,
      rotate: 360,
      ease: "expoScale",
      scrollTrigger: {
        trigger: ".icon",
        start: "top 380px",
        end: "-200px",
        scrub: 3,
      },
    });
  });
</script>

<div class="wrapper-list">
  <div class="wrapper-icon">
    <!-- <img src={icon} alt="" class="icon" /> -->
<img src={icon} alt="" class="icon">
  </div>
  <div class="p"><span>{title}</span>{p}</div>
</div>

<style>
  .wrapper-list {
    display: flex;
    flex-direction: row;
    margin: 20px;
    font-family: epilogue;
    color: var(--bg);
    width: 100%;
  }
  .wrapper-icon {
    display: flex;
    justify-content: center;
    align-items: center;
    filter: drop-shadow(3px 6px 15px rgba(0, 0, 0, 0.406));
    margin-right: 20px;
  }
  .icon {
     filter: drop-shadow(1px 1px 3px rgba(0, 0, 0, 0.437));
    height: 80px;
    width: 80px;
    border-radius: 50%;
    /* background-color: var(--primary); */
    /* clip-path: polygon(70% 0, 100% 11%, 85% 38%, 96% 67%, 82% 89%, 16% 99%, 0 65%, 11% 44%, 16% 15%); */
    transform: translateX(-300px);
    fill: blue;
  }
  @keyframes anim {
    from {
        stroke-dashoffset: 2000px;
    }
    to {
        stroke-dashoffset: 0px;
    }
}
  .p {
    font-size: 1.2em;
    font-family: epilogue;
    color: var(--bg);
    font-weight: 400;
    list-style: none;
    padding: 10px;
  }
  .p span {
    font-weight: 800;
    color: transparent;
    -webkit-background-image: linear-gradient(to left, var(--blue), var(--ca));
    background-image: linear-gradient(to left, var(--blue), var(--ca));
    -webkit-background-clip: text;
    background-clip: text;
  }
  @media screen and (max-width: 768px) {
    .wrapper-list {
      flex-direction: column;
      align-items: center;
      justify-content: center;
      margin: 0px;
    }
    .wrapper-icon {
      margin-bottom: 20px;
    }
  }
</style>
