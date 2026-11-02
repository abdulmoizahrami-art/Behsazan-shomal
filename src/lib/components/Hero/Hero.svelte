<script lang="ts">
	import './Hero.css';
	import { site } from '../../data/site';
	import Button from '../Button/Button.svelte';
	import Icon from '../Icon/Icon.svelte';

	// با کلیک روی هر دکمه، رنگ دو دکمه جابه‌جا می‌شود (همیشه فقط یکی روشن است)
	let swapped = $state(false);
</script>

<header class="hero" id="top">
	<img class="hero__art hero__art--left" src="/images/building.jpg" alt="" aria-hidden="true" />
	<img class="hero__art hero__art--right" src="/images/building.jpg" alt="" aria-hidden="true" />

	<div class="hero__body">
		<img class="hero__logo" src="/images/logo.png" alt="لوگوی {site.name}" width="168" height="186" />
		<h1 class="hero__title">{site.name}</h1>
		<p class="hero__group">{site.group}</p>
		<p class="hero__slogan">{site.slogan}</p>

		<div class="hero__actions" onclick={() => (swapped = !swapped)} role="presentation">
			<Button href="#contact" variant={swapped ? 'outline' : 'solid'}>تماس بگیرید</Button>
			<Button href="#services" variant={swapped ? 'solid' : 'outline'}>خدمات ما</Button>
		</div>
	</div>

	<a class="hero__cue" href="#about">
		<span>بیشتر ببینید</span>
		<Icon name="chevron" />
	</a>
</header>
