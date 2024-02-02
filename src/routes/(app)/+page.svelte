<script lang="ts">
	import TPose from '$lib/TPose.svelte';

	import aTPoseGIF from '$lib/assets/gifs/a-tpose.gif';
	import oTPoseGIF from '$lib/assets/gifs/o-tpose.gif';
	import nahabaMainJPG from '$lib/assets/nahaba_main_1x1.jpg';
	import bloodMP4 from '$lib/assets/blood.mp4';

	import { onMount } from 'svelte';

	onMount(() => {
		document.body.style.overflowY = 'hidden';
	});
</script>

<svelte:head>
	<title>Український гурт NAHABA</title>
	<meta
		name="description"
		content="NAHABA - дует який дивує кожним аспектом своєї творчості. Вони об'єднують фолькльорні мотиви та екстрім вокал, прокляття та кавери на Курган і Агрегат. Ці музиканти не бояться вразити натовп, навіть більше, налякати його."
	/>
</svelte:head>

<div class="center-container">
	<div class="image-container">
		<img src={nahabaMainJPG} alt="Members of NAHABA band" />
		<video id="blood-video" muted playsinline autoplay loop>
			<source src={bloodMP4} />
		</video>
	</div>
	<a class="listen-now" href="https://song.link/nahaba_glasss" target="_blank">Listen now</a>
</div>

<div class="tpose-container">
	<TPose src={aTPoseGIF} character="A" />
	<TPose src={oTPoseGIF} character="O" />
</div>

<style>
	.tpose-container {
		bottom: 0;
		display: flex;
		width: 100%;
		justify-content: space-between;

		@media (min-width: 700px) {
			position: fixed;
		}
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

		width: 80vw;

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
