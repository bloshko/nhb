<script>
	import nahabaLogoSVG from '$lib/assets/nahaba_logo.svg';
</script>

<header>
	<a href="/"><img src={nahabaLogoSVG} alt="NAHABA band logo" width="64" /></a>
	<nav>
		<a href="/">Хоум</a>
		<a href="/videos">Відео</a>
	</nav>
</header>

<style>
	header {
		display: flex;
		padding-bottom: 16px;
		justify-content: space-between;
		align-items: center;
		width: 100%;
		max-width: 2500px;
		padding: 16px;

		@media (min-width: 1000px) {
			padding: 64px;
		}
	}
	nav {
		display: flex;
		gap: 12vw;
		align-items: center;
		justify-content: flex-end;
	}
</style>
