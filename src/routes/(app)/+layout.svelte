<script>
	import Header from '$lib/Header.svelte';
	import Head from '$lib/Head.svelte';
</script>

<Head />
<Header />
<main>
	<slot />
</main>
<div class="background-gradient" />

<style>
	main {
		display: flex;
		flex-direction: column;
		align-items: center;
		width: 100%;
		max-width: 2500px;
		position: relative;
		justify-self: center;
	}
	.background-gradient {
		position: fixed;
		width: 100vw;
		height: 100vh;
		background: linear-gradient(180deg, rgba(0, 0, 0, 0) 0%, rgba(0, 0, 0, 1) 50%);
		z-index: -2;
	}
	:global(body) {
		min-height: 100svh;
		background-image: url('/bg.png');
		background-attachment: fixed;
		background-repeat: no-repeat;
		background-color: black;
		background-size: cover;
		background-position: center center;
		margin: 0;

		grid-template-rows: 20vh 5fr;
		display: grid;
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
