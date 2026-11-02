<script lang="ts">
	import { paths } from './paths';

	let { name, label = '' }: { name: keyof typeof paths; label?: string } = $props();
</script>

<svg class="icon" viewBox="0 0 24 24" role={label ? 'img' : undefined} aria-label={label || undefined} aria-hidden={label ? undefined : 'true'}>
	<path d={paths[name]} />
</svg>
