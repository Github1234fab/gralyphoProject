<script>
  import { onMount } from "svelte";
  export let title;
  export let lien;
  export let i;

  onMount(() => {
    const cards = document.querySelectorAll(".card-services");
    cards.forEach((el) => {
      gsap.to(el, {
        y: 0,
        ease: "ease-in-out",
        scrub: 5,
        scrollTrigger: {
          trigger: el,
          start: "top 700px",
          end: "-1000px",
          scrub: 5,
        },
      });
    });
  });
</script>

<div class="card-services">
  <h2>{title}</h2>
  <a href={lien}><div class="icon">{i}</div> </a>
</div>

<style>
  .card-services {
    transform: translateY(300px);
    display: flex;
    align-items: center;
    justify-content: center;
    flex-direction: column;
    background-color: var(--primary);
    box-shadow: 0px 0px 10px black;
    width: 400px;
    height: 300px;
  }
  .card-services h2 {
    font-family: epilogue;
    color: white;
    font-size: var(--m);
    text-transform: capitalize;
    text-align: center;
  }
  .icon {
    transition: 0.7s ease-in-out;
    color: white;
    font-size: 3.4em;
    z-index: 2;
  }
  .icon:hover {
    animation: bounce 0.4s ease-in-out;
  }

  @media screen and (min-width: 1400px) and (max-width: 2500px) {
  }

  @media screen and (min-width: 1200px) and (max-width: 1400px) {
  }

  @media screen and (min-width: 992px) and (max-width: 1200px) {
  }

  @media screen and (min-width: 768px) and (max-width: 992px) {
  }

  @media screen and (min-width: 576px) and (max-width: 767px) {
  }

  @media screen and (min-width: 300px) and (max-width: 575px) {
    .card-services {
      transform: translateY(300px);
      width: 300px;
      height: 250px;
    }
  }
</style>
