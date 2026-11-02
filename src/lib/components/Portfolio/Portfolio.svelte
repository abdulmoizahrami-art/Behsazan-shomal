<script lang="ts">
	import './Portfolio.css';
	import { site } from '../../data/site';
	import Icon from '../Icon/Icon.svelte';
</script>

<section id="portfolio" class="section">
	<div class="container">
		<h2 class="section-title gold">نمونه کارها</h2>
		<p class="section-lead">برخی از پروژه‌های ما</p>

		<ul class="portfolio__grid">
			{#each site.projects as p}
				<li class="gold-card portfolio__item">
					<div class="portfolio__photo">
						{#if p.image}
							<img src={p.image} alt={p.title} loading="lazy" />
						{:else}
							<Icon name="build" />
						{/if}
					</div>
					<h3>{p.title}</h3>
					<p>{p.text}</p>
				</li>
			{/each}
		</ul>
	</div>
</section>
