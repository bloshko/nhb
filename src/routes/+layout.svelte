<script>
	import Header from '$lib/Header.svelte';
</script>

<Header />
<main>
	<slot />
</main>

<style>
	main {
		display: flex;
		flex-direction: column;
		align-items: center;
		width: 100%;
		max-width: 2500px;
		position: relative;
	}
	:global(body) {
		min-height: 100svh;
		background-image: url('/bg.png');
		background-attachment: fixed;
		background-repeat: no-repeat;
		background-color: black;
		background-size: cover;
		background-position: center center;

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
