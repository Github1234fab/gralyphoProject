<script>
  import "./styles.css";
  import Footer from "../sections/Footer.svelte";

</script>

<main>
  <slot />
  <Footer />
</main>


<style>
  main {
 background-color: var(--primary);
    overflow: hidden;
    height: auto; 
    scroll-behavior: smooth; 
  }
  
</style>
