<script lang="ts">
	import './Footer.css';
	import { site } from '../../data/site';
</script>

<footer class="footer">
	<div class="container footer__row">
		<span class="footer__brand">
			<img src="/images/logo.png" alt="" width="30" height="33" />
			© {site.name} — تمام حقوق محفوظ است
		</span>
		<span>{site.partner}</span>
	</div>
</footer>
