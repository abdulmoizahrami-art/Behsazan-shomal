<script lang="ts">
	import './Services.css';
	import { site } from '../../data/site';
	import Icon from '../Icon/Icon.svelte';
</script>

<section id="services" class="section services">
	<div class="container">
		<h2 class="section-title gold">خدمات ما</h2>

		<ul class="services__list">
			{#each site.services as s}
				<li class="services__card gold-card">
					<span class="services__icon"><Icon name={s.icon as 'home'} /></span>
					<h3>{s.title}</h3>
					<p>{s.text}</p>
					<a href="#contact">
						<Icon name="arrow" /> بیشتر بدانید
					</a>
				</li>
			{/each}
		</ul>
	</div>
</section>
