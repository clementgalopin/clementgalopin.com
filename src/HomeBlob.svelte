<script>
	export let blobId = 0;
</script>

<div class="blob" id={"blobSvg"+blobId}>
	<svg viewBox="0 0 500 500" xmlns="http://www.w3.org/2000/svg" xmlns:xlink="http://www.w3.org/1999/xlink">
		<defs>
			<linearGradient id={"gradient"+blobId} x1="0%" y1="0%" x2="0%" y2="100%">
			{#if blobId === 1}
			<stop offset="0%" style="stop-color: rgb(194, 229, 156);"></stop>
			<stop offset="100%" style="stop-color: rgb(100, 179, 244);"></stop>
			{:else if blobId === 2}
			<stop offset="0%" style="stop-color: rgb(238, 205, 163);"></stop>
			<stop offset="100%" style="stop-color: rgb(239, 98, 159);"></stop>
			{:else}
			<stop offset="0%" style="stop-color: rgb(76, 161, 175);"></stop>
			<stop offset="100%" style="stop-color: rgb(196, 224, 229);"></stop>
			{/if}
			</linearGradient>
		</defs>
		{#if blobId === 1}
		<path id={"blob"+blobId} d="M443.5,307.5Q450,365,411,413Q372,461,311,451Q250,441,212.5,410.5Q175,380,120,368.5Q65,357,33,303.5Q1,250,27,193Q53,136,100,103.5Q147,71,198.5,42.5Q250,14,294,55.5Q338,97,367.5,131Q397,165,417,207.5Q437,250,443.5,307.5Z" fill={"url(#gradient"+blobId+")"}></path>
		{:else if blobId === 2}
		<path id={"blob"+blobId} d="M440.5,292.5Q382,335,351.5,370Q321,405,274.5,403.5Q228,402,182,391.5Q136,381,114.5,338.5Q93,296,66,242Q39,188,72.5,136Q106,84,165,78Q224,72,279,69.5Q334,67,396,91.5Q458,116,478.5,183Q499,250,440.5,292.5Z" fill={"url(#gradient"+blobId+")"}></path>
		{:else}
		<path id={"blob"+blobId} d="M432.5,295.5Q392,341,364.5,390.5Q337,440,278.5,448Q220,456,154.5,446Q89,436,90.5,366Q92,296,79.5,246Q67,196,108.5,165.5Q150,135,189,114.5Q228,94,272.5,98.5Q317,103,383,112.5Q449,122,461,186Q473,250,432.5,295.5Z" fill={"url(#gradient"+blobId+")"}></path>
		{/if}
	</svg>
</div>

<style>
	.blob {
		position: absolute;
		transition: all 0.5s ease-in-out;
		opacity: 0.45;
	}
	.blob, .blob svg {
		height: 100%;
		width: 100%;
	}
	#blobSvg0 {
		z-index: -2;
		left: -25%;
		top: -15%;
		animation: morph0 8s ease-in-out infinite;
	}
	#blobSvg1 { 
		z-index: -3;
		left: 5%;
		top: 25%;
		animation: morph1 8s ease-in-out infinite;
	}
	#blobSvg2 {
		z-index: -4;
		left: 25%;
		top: -15%;
		animation: morph2 16s ease-in-out infinite;
	}
	@keyframes morph0 {
		0% {
			width:95%;
			transform: rotate(5deg);
		} 
		50% {
			width:90%;
			transform: rotate(15deg);
		}
		100% {
			width:95%;
			transform: rotate(5deg);
		}
	}
	@keyframes morph1 {
		0% {
			width:95%;
			transform: rotate(-15deg);
		} 
		50% {
			width:90%;
			transform: rotate(-30deg);
		}
		100% {
			width:95%;
			transform: rotate(-15deg);
		}
	}
	@keyframes morph2 {
		0% {
			width:95%;
			transform: rotate(15deg);
		} 
		50% {
			width:90%;
			transform: rotate(30deg);
		}
		100% {
			width:95%;
			transform: rotate(15deg);
		}
	}
</style>