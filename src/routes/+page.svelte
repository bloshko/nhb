<script>
	import Head from '$lib/Head.svelte';
</script>

<Head />

<div class="center-container">
	<img src="/nahaba_main_1x1.jpg" alt="main img" />
	<a class="listen-now" href="https://song.link/nahaba_glasss" target="_blank">Listen now</a>
</div>

<style>
	.center-container {
		display: flex;
		flex-direction: column;
		justify-content: center;
		align-items: center;
		gap: 32px;
		width: 100%;
	}
	img {
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
	.listen-now {
		font-size: 18px;
		padding: 24px 32px;
		border: 1px solid #f20523;
		color: #f20523;
		text-transform: uppercase;
		text-align: center;
		max-width: 300px;
		width: 100%;
	}
	.listen-now:hover {
		background-color: #f20523;
		color: black;
		transition: all 0.5s;
	}
</style>
