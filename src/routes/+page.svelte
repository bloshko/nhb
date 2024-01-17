<script>
	import Header from '$lib/Header.svelte';
</script>

<Header />
<main>
	<div class="center-container">
		<img class="main-img" src="nahaba_main_1x1.jpg" alt="main img" />
		<a class="listen-now" href="https://song.link/nahaba_glasss" target="_blank">Listen now</a>
	</div>
</main>

<style>
	main {
		display: flex;
		flex-direction: column;
		justify-content: center;
		align-items: center;
		width: 100%;
		max-width: 2500px;
		position: relative;
	}
	.center-container {
		display: flex;
		flex-direction: column;
		justify-content: center;
		align-items: center;
		position: absolute;
		transform: translateX(-50%) translateY(-50%);
		gap: 32px;
		top: 50%;
		left: 50%;
	}
	.main-img {
		width: 30vw;
		min-width: 450px;
		max-width: 700px;
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
	:global(body) {
		height: 100svh;
		background-image: url('bg.png');
		background-attachment: scroll;
		display: flex;
		justify-content: center;
	}
	:global(html) {
		box-sizing: border-box;
	}
	:global(a) {
		text-decoration: none;
		font-size: 18px;
		color: white;
	}
	:global(*) {
		box-sizing: border-box;
		font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
		margin: 0;
	}
</style>
