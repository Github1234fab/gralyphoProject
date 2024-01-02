
<script>
	// import "../app.pcss";
	import './styles.css';
	import Header from '../sections/Header.svelte';
	import Asection from '../sections/Asection.svelte';
	import Bsection from '../sections/Bsection.svelte';
	import Csection from '../sections/Csection.svelte';
	import DSection from '../sections/DSection.svelte';
	import ESection from '../sections/ESection.svelte';
	import FSection from '../sections/FSection.svelte';
	import GSection from '../sections/GSection.svelte';
	import HSection from '../sections/HSection.svelte';
	// import ISection from '../sections/ISection.svelte';
	import JSection from '../sections/JSection.svelte';
	import Footer from '../sections/Footer.svelte';
</script>

<main>
<Header/>
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

	<Footer />
</main>

<!-- <slot /> -->

<style>
	main {
		background-color: var(--colorO);
		overflow: hidden;
	}
</style>
