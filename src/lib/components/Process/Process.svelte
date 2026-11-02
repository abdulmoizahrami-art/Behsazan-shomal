<script lang="ts">
	import './Process.css';
	import { site } from '../../data/site';

	const digits = ['۱', '۲', '۳', '۴', '۵', '۶'];
</script>

<section id="process" class="section">
	<div class="container">
		<h2 class="section-title gold">مراحل کار</h2>
		<p class="section-lead">از اولین گفتگو تا تحویل کلید</p>

		<ol class="process__steps">
			{#each site.steps as step, i}
				<li>
					<span class="process__num">{digits[i]}</span>
					<h3>{step.title}</h3>
					<p>{step.text}</p>
				</li>
			{/each}
		</ol>
	</div>
</section>
