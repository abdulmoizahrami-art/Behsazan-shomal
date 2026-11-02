<script lang="ts">
	import './Nav.css';
	import { site } from '../../data/site';

	let active = $state('');

	// لینکی که کاربر الان در بخش آن است را مشخص می‌کند
	$effect(() => {
		const observer = new IntersectionObserver(
			(entries) => entries.forEach((e) => e.isIntersecting && (active = e.target.id)),
			{ rootMargin: '-40% 0px -55% 0px' }
		);
		site.nav.forEach(({ id }) => {
			const el = document.getElementById(id);
			if (el) observer.observe(el);
		});
		return () => observer.disconnect();
	});
</script>

<nav class="nav" aria-label="منوی اصلی">
	<a class="nav__brand" href="#top">
		<img src="/images/logo.png" alt="" width="46" height="51" />
		{site.name}
	</a>

	<ul class="nav__links">
		{#each site.nav as link}
			<li>
				<a href="#{link.id}" class:is-active={active === link.id}>{link.label}</a>
			</li>
		{/each}
	</ul>

	<a class="nav__cta" href="#contact">تماس با ما</a>
</nav>
