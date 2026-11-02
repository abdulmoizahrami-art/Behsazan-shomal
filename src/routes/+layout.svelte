<script lang="ts">
	import '@fontsource-variable/vazirmatn';
	import '../app.css';
	import type { LayoutProps } from './$types';

	let { children }: LayoutProps = $props();
</script>

{@render children()}
