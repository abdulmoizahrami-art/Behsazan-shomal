<script lang="ts">
	import './Button.css';
	import type { Snippet } from 'svelte';

	let {
		href,
		variant = 'solid',
		children
	}: { href: string; variant?: 'solid' | 'outline'; children: Snippet } = $props();
</script>

<a class="btn btn--{variant}" {href}>{@render children()}</a>
