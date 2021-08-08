<script>
	import HomeDescription from './HomeDescription.svelte';
	import HomeHeader from './HomeHeader.svelte';
	import HomeFooter from './HomeFooter.svelte';
	import HomeBlob from './HomeBlob.svelte';
</script>

<main>
	<div class="glass">
		<HomeHeader />
		<HomeDescription />
		<HomeBlob blobId={0} />
		<HomeBlob blobId={1} />
		<HomeBlob blobId={2} />
	</div>
	<HomeFooter />
</main>

<style global lang="postcss">
	@tailwind base;
	@tailwind components;
	@tailwind utilities;

	@import url('https://fonts.googleapis.com/css?family=Lora:400,700|Source+Sans+Pro:300,400|Dosis:300,400,700');

	:root {
		--link-color: #007FFF; /* slateblue */
		--dark-grey: #36363C;
	}

	*, *:before, *:after {
		box-sizing: border-box;
		margin: 0;
		padding: 0;
		font-family: "Source Sans Pro", sans-serif;
		color: #fff;
	}
	html, body {
		width: 100%;
		height: 100%;
		overflow: hidden;
	}
	body {
		display: flex;
		align-items: center;
		justify-content: center;
		background-color: var(--dark-grey);
	}

	main {
		position: relative;
		padding: 1em;
		width: 550px;
		max-width: 90vw;
		margin: 0 auto;
		
	}

	p {
		font-weight: 300;
		@apply text-xl;
	}
	div + p, p + p {
		margin-top: calc(2/3 * 1em);
	}

	.glass {
		@apply p-6;
		width: 100%;
		height: 100%;
		background: rgba(255, 255, 255, 0.15);
		border-radius: 16px;
		box-shadow: 0 4px 30px rgba(0, 0, 0, 0.1);
		backdrop-filter: blur(5px);
		-webkit-backdrop-filter: blur(5px);
		border: 1px solid rgba(255, 255, 255, 0.3);
	}
</style>