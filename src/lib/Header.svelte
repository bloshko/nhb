<header>
	<a href="/"><img src="/nahaba_logo.svg" alt="nahaba logo" width="64" /></a>
	<nav>
		<a href="/">HOME</a>
		<a href="#">VIDEOS</a>
	</nav>
</header>

<style>
	header {
		position: fixed;
		padding: 64px;
		padding-bottom: 16px;
		display: flex;
		justify-content: space-between;
		width: 100%;
		max-width: 2500px;

		@media (max-width: 1000px) {
			position: initial;
			padding: 16px;
		}
	}
	nav {
		display: flex;
		gap: 12vw;
		align-items: center;
		justify-content: flex-end;
	}
</style>
