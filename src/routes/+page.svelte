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
  import SectionSocial from "../sections/SectionSocial.svelte";
  import BeneficeSection from "../sections/BeneficeSection.svelte";
  import ActionSection from "../sections/ActionSection.svelte";
</script>

<main in:fade={{ duration: 2000 }}>

  <HSection />
<SectionSocial/>
 <BeneficeSection />
   <JSection />
  <Csection />
    <DSection />
   
  <!-- <SectionValue /> -->
 

  <section id="sectionE">
    <ESection />
  </section>

      <GSection />

  <section id="sectionA">
    <ActionSection />
  </section>
</main>

<style>
  main {
    overflow: hidden;
  }
</style>
