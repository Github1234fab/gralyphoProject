<script>
  // export let icon;
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
  <p class="title"><span>{title}</span><br></p> 
<p>{p}</p>
</div>

<style>
  .wrapper-list {
    display: flex;
    flex-direction:column;
    margin: 20px;
    font-family: epilogue;
    color: var(--bg);
    width: 60%;
  }
 
  @keyframes anim {
    from {
        stroke-dashoffset: 2000px;
    }
    to {
        stroke-dashoffset: 0px;
    }
}
  p {
    font-size: 1.2em;
    font-family: epilogue;
    color: var(--bg);
    font-weight: 300;
    list-style: none;
    padding: 10px;
    text-align: left;
  }
  .title {
    font-weight: 600;
    /* color: transparent;
    -webkit-background-image: linear-gradient(to left, var(--blue), var(--ca));
    background-image: linear-gradient(to left, var(--blue), var(--ca));
    -webkit-background-clip: text;
    background-clip: text; */

  }
  @media screen and (max-width: 768px) {
    .wrapper-list {
      flex-direction: column;
      align-items: center;
      justify-content: center;
      margin: 0px;
    }

  }
</style>
