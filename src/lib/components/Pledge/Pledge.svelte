<script lang="ts">
	import './Pledge.css';
	import { site } from '../../data/site';

	const { title, slogan, lines } = site.pledge;
</script>

<section id="pledge" class="pledge">
	<div class="container pledge__grid">
		<div>
			<h2 class="pledge__title">{title}</h2>
			<p class="pledge__slogan gold">{slogan}</p>
		</div>
		<p class="pledge__lines">
			{#each lines as line}{line}<br />{/each}
		</p>
	</div>
</section>
