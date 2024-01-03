<script>
  import "./styles.css";
  import Footer from "../sections/Footer.svelte";
</script>

<nav class="navigation">
  <a href="/">Home</a>
  <a href="/Sites">Sites Web</a>
  <a href="/Applications">Application</a>
</nav>

<main>
  <slot />
  <Footer />
</main>

<style>
  main {
    background-color: var(--colorO);
    overflow: hidden;
  }
  .navigation {
    background-color: var(--colorO);
    display: flex;
    justify-content: space-around;
    padding: 30px;
  }
  a {
    color: white;
    text-decoration: none;
    transition: 0.3s ease-in-out;
    font-weight: 500;
  }
  a:hover {
    color: var(--colorD);
  }

</style>
