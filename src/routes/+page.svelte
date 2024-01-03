<script>
  import "./styles.css";
  import Asection from "../sections/Asection.svelte";
  import Bsection from "../sections/Bsection.svelte";
  import Csection from "../sections/Csection.svelte";
  import DSection from "../sections/DSection.svelte";
  import ESection from "../sections/ESection.svelte";
  import FSection from "../sections/FSection.svelte";
  import GSection from "../sections/GSection.svelte";
  import HSection from "../sections/HSection.svelte";
  import JSection from "../sections/JSection.svelte";
  import { fade, slide } from "svelte/transition";
</script>

<main in:fade={{duration:2000}}>
  <!-- <slot /> -->
  <!-- <Header /> -->
  <section id="sectionA">
    <Asection />
    <Bsection />
    <Csection />
    <JSection />
    <DSection />
    <section id="sectionE">
      <ESection />
    </section>
    <section id="sectionF">
      <FSection />
    </section>
    <GSection />
    <HSection />
  </section>
</main>

<style>
  main {
    background-color: var(--colorO);
    overflow: hidden;
  }
</style>
