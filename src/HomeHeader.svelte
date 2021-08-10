<div class="inline-flex space-x-4 items-center">
	<div class="rounded-full h-24 w-24 avatar-clement">
		<div class="rounded-full bg-gradient-to-r from-yellow-400 via-red-500 to-pink-500"></div>
	</div>
	<div>
		<p>Hello, <span class="md:hidden"><br></span>I'm <b>Clément</b> 👋</p>
	</div>
</div>

<style>
	div.avatar-clement {
		position: relative;
		background-image: url('/clement.png');
		background-size: cover;
		border: 2px solid var(--link-color);
	}
	div.avatar-clement > div {
		position: absolute;
		z-index: -1;
		width: 100%;
		height: 100%;
	}
</style>