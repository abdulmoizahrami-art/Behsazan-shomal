<script lang="ts">
	import './Contact.css';
	import { site } from '../../data/site';
	import Button from '../Button/Button.svelte';
	import Icon from '../Icon/Icon.svelte';

	const c = site.contact;
	const rows = [
		{ icon: 'pin', label: 'آدرس', value: c.address, href: null },
		{ icon: 'phone', label: 'تلفن', value: c.phone, href: c.phoneHref },
		{ icon: 'mail', label: 'ایمیل', value: c.email, href: `mailto:${c.email}` }
	] as const;
</script>

<section id="contact" class="section contact">
	<div class="container contact__grid">
		<div>
			<h2 class="section-title gold">تماس با ما</h2>
			<p class="section-lead">برای مشاوره و برآورد، با ما در تماس باشید.</p>

			<ul class="contact__rows">
				{#each rows as r}
					<li>
						<svelte:element this={r.href ? 'a' : 'div'} class="contact__row" href={r.href ?? undefined}>
							<span class="contact__icon"><Icon name={r.icon} /></span>
							<span>
								<small>{r.label}</small>
								<bdi>{r.value}</bdi>
							</span>
						</svelte:element>
					</li>
				{/each}
			</ul>
		</div>

		<div class="contact__cta gold-card">
			<h3>{c.ctaTitle}</h3>
			<p>{c.ctaText}</p>
			<div class="contact__actions">
				<Button href={c.phoneHref}>زنگ بزنید</Button>
				<Button href="mailto:{c.email}" variant="outline">ایمیل بفرستید</Button>
			</div>
		</div>
	</div>
</section>
