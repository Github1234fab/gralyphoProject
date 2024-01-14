<script>
  import "./styles.css";
  import Asection from "../sections/Asection.svelte";
  import SectionTestimony from "../sections/SectionCent.svelte";
  import Csection from "../sections/Csection.svelte";
  import DSection from "../sections/DSection.svelte";
  import ESection from "../sections/ESection.svelte";
  import FSection from "../sections/FSection.svelte";
  import GSection from "../sections/GSection.svelte";
  import HSection from "../sections/HSection.svelte";
  import JSection from "../sections/JSection.svelte";
  import SectionValue from "../sections/SectionValue.svelte";
  import { fade, slide } from "svelte/transition";
</script>

<main in:fade={{ duration: 2000 }}>
  <section id="sectionA">
    <Asection />
  </section>
  <SectionValue />
  <Csection />
  <JSection />
  <section id="sectionE">
    <ESection />
  </section>
  <DSection />
  <HSection />
  <GSection />
</main>

<style>
  main {
    overflow: hidden;
  }
</style>
