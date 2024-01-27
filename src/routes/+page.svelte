<script lang="ts">
	import Head from '$lib/Head.svelte';
	import TPose from '$lib/TPose.svelte';
	import { onMount } from 'svelte';

	onMount(() => {
		document.body.style.overflowY = 'hidden';
	});
</script>

<Head />

<div class="center-container">
	<div class="image-container">
		<img src="/nahaba_main_1x1.jpg" alt="main img" />
		<video id="blood-video" muted playsinline autoplay loop>
			<source src="/blood.mp4" />
		</video>
	</div>
	<a class="listen-now" href="https://song.link/nahaba_glasss" target="_blank">Listen now</a>
</div>

<div class="tpose-container">
	<TPose src="/gifs/a-tpose.gif" />
	<TPose src="/gifs/o-tpose.gif" />
</div>

<style>
	.tpose-container {
		display: flex;
		width: 100%;
		justify-content: space-between;
	}
	.center-container {
		display: flex;
		flex-direction: column;
		justify-content: center;
		align-items: center;
		gap: 32px;
		width: 100%;
	}
	.image-container {
		position: relative;
		line-height: 0;

		width: 100vw;
		@media (min-width: 700px) {
			width: 80vw;
		}

		@media (min-width: 1000px) {
			width: 30vw;
		}

		@media (min-width: 1600px) {
			width: 30vw;
			min-width: 450px;
			max-width: 700px;
		}
	}
	video {
		position: absolute;
		width: 100%;
		bottom: 0;
		left: 0;
		transform: translateY(100%);
		z-index: -1;
		filter: brightness(0.8);
	}
	img {
		width: 100%;
		z-index: 2;
	}
	.listen-now {
		font-size: 18px;
		padding: 24px 32px;
		border: 1px solid #f20523;
		color: #f20523;
		text-transform: uppercase;
		text-align: center;
		max-width: 300px;
		width: 100%;
		z-index: 1;
	}
	.listen-now:hover {
		background-color: #f20523;
		color: black;
		transition: all 0.5s;
	}
</style>
