<script>
	let year = new Date().getFullYear();
</script>

<div>
	<p class="text-center">&copy; {year} Clément Galopin. Built with Svelte, Tailwind & Netlify.</p>
</div>

<style>
	p {
		@apply p-3;
		font-weight: 100;
		line-height: calc(3/2 * 0.35em);
		font-size: 0.7rem;
	}
</style>