<script>
	let year = new Date().getFullYear();
</script>

<div>
	<p class="text-center">&copy; {year} Clément Galopin. <span class="md:hidden"><br></span>I built this with Svelte, Tailwind & Vercel.</p>
</div>

<style>
	p {
		@apply p-3;
		@apply text-xs;
		font-weight: 100;
	}
</style>