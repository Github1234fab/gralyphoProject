<script>
  import "./styles.css";
  import Footer from "../sections/Footer.svelte";

</script>

<main>
  <slot />
  <div id="footer">
  <Footer />
  </div>
</main>


<style>
  main {
 background-color: var(--primary);
    overflow: hidden;
    height: auto; 
    scroll-behavior: smooth; 
  }
  
</style>
