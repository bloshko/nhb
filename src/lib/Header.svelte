<script lang="ts">
	import nahabaLogoSVG from '$lib/assets/nahaba_logo.svg';
	import homeSVG from '$lib/assets/home.svg';
	import videosSVG from '$lib/assets/videos.svg';
	import merchSVG from '$lib/assets/merch.svg';
	import { page } from '$app/stores';
</script>

<header>
	<a href="/"><img src={nahabaLogoSVG} alt="NAHABA band logo" /></a>
	<nav>
		<a href="/" class:active={$page.url.pathname === '/'}>
			<img src={homeSVG} alt="home" />
		</a>
		<a href="/videos" class:active={$page.url.pathname === '/videos'}>
			<img src={videosSVG} alt="videos" />
		</a>
		<a href="/merch" class:active={$page.url.pathname === '/merch'}>
			<img src={merchSVG} alt="merch" />
		</a>
	</nav>
</header>

<style>
	img {
		width: 45px;

		@media (min-width: 700px) {
			width: unset;
			height: 64px;
		}
	}
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
	a {
		transition: all 0.5s;
	}
	a:hover {
		transform: scale(2, 0.5);
	}
	.active {
		transform: scale(2, 0.5);
	}
	nav {
		display: flex;
		gap: 12vw;
		align-items: center;
		justify-content: flex-end;
	}
</style>
