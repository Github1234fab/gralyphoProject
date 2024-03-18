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
          start: "top 900px",
          end: "-1000px",
          scrub: 5,
        },
      });
    });
  });
</script>


<div class="card-services">
  <h2>{title}</h2>
  <a href={lien}><i class="{i} icon"></i> </a>
</div>


<style>
 
 .card-services {
    transform: translateY(300px);
    display: flex;
    align-items: center;
    justify-content: center;
    flex-direction: column;
    background-color: var(--CTA);
    box-shadow: 0px 0px 15px rgba(0, 0, 0, 0.299);
    /* width: 400px;
    height: 200px; */
    border-radius: 100px;
    padding: 20px;
  }
  .card-services h2 {
    font-family: poppins;
    font-weight: 600;
    color: white;
    font-size: var(--m);
    text-transform: capitalize;
    text-align: center;
  }
  .icon {
    margin-top: 10px;
    transition: 0.7s ease-in-out;
    color: var(--CTA);
    font-size: 3.4em;
    z-index: 2;
    text-shadow: -2px -2px 10px rgba(150, 78, 1, 0.668), 2px 2px 10px rgba(0, 0, 0, 0.5);
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
   @media screen and (min-width: 300px) and (max-width: 576px) {


  }


</style>
