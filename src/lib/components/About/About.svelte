<script lang="ts">
	import './About.css';
	import { site } from '../../data/site';
	import Icon from '../Icon/Icon.svelte';

	const { paragraphs, badge, railIcons } = site.about;
</script>

<section id="about" class="section about">
	<div class="container about__grid">
		<div class="about__text">
			<h2 class="section-title">درباره ما</h2>
			<p><strong>{site.name}</strong> {paragraphs[0]}</p>
			<p>{paragraphs[1]}</p>

			<div class="about__badge">
				<p><strong>{site.name}</strong> {badge}</p>
				<Icon name="medal" />
			</div>
		</div>

		<ul class="about__rail" aria-hidden="true">
			{#each railIcons as icon}
				<li><Icon name={icon as 'crane'} /></li>
			{/each}
		</ul>
	</div>
</section>
