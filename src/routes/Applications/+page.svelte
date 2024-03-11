<script>
  import { fade, slide } from "svelte/transition";
  // import bg from "../../Assets/png-gralypho/41.png";
  import Header from "../../sections/Header.svelte";
</script>

<Header />
<section class="application-section" in:fade={{ duration: 3000 }}>

<div class="wrapper-testimonial">
<h2>"La seule limite à ce que vous pouvez réaliser est celle que vous imaginez." </h2>
<h3>Roy T. Bennett</h3>
</div>













</section>

<style>
.application-section {
 display:grid;
  grid-template-columns: repeat(12, 1fr);
  grid-template-rows: auto;
  height: auto;
  font-size: 16px;

  } 

  
  .wrapper-testimonial {
    display: flex;
    justify-content: center;
    align-items: center;
    flex-direction: column;
    margin-top: 50px;
    margin-bottom: 50px;
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
  section {
    display: grid;
    grid-template-columns: repeat(12, 1fr);
    grid-template-rows: auto;
    /* background-color: var(--colorO); */
    height: 100%;
    width: 100%;
    margin-top: 30px;
    margin-bottom: 50px;
  }
 

@media screen and (min-width: 1400px) and (max-width: 2500px){


}

@media screen and (min-width: 1200px) and (max-width: 1400px){


}


@media screen and (min-width: 992px) and (max-width: 1200px){


}

@media screen and (min-width: 768px) and (max-width: 992px){


}

@media screen and (min-width: 576px) and (max-width: 767px){


}

@media screen and (min-width: 300px) and (max-width: 575px){


}


</style>
