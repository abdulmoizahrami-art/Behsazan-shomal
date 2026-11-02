<script lang="ts">
	import { site } from '../lib/data/site';
	import Nav from '../lib/components/Nav/Nav.svelte';
	import Hero from '../lib/components/Hero/Hero.svelte';
	import About from '../lib/components/About/About.svelte';
	import Services from '../lib/components/Services/Services.svelte';
	import Portfolio from '../lib/components/Portfolio/Portfolio.svelte';
	import Process from '../lib/components/Process/Process.svelte';
	import Pledge from '../lib/components/Pledge/Pledge.svelte';
	import Contact from '../lib/components/Contact/Contact.svelte';
	import Footer from '../lib/components/Footer/Footer.svelte';
</script>

<svelte:head>
	<title>{site.name} | {site.group}</title>
	<meta name="description" content="{site.name} — {site.group} در شمال افغانستان. طراحی، ساخت، تهیهٔ مصالح و بازسازی. {site.slogan}." />
	<meta property="og:title" content="{site.name} | {site.group}" />
	<meta property="og:image" content="/images/logo.png" />
</svelte:head>

<Nav />
<main>
	<Hero />
	<About />
	<Services />
	<Portfolio />
	<Process />
	<Pledge />
	<Contact />
</main>
<Footer />
