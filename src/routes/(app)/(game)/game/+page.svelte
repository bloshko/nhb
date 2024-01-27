<script lang="ts">
	import { onMount } from 'svelte';

	let src: string;

	onMount(() => {
		const search = window.location.search;
		src = new URL(search, 'https://web-game-5ak.pages.dev/').toString();
	});
</script>

<iframe {src} title="nahaba game" />

<style>
	iframe {
		border: 0;
		min-width: 100svw;
		min-height: 100svh;
	}
	:global(body) {
		margin: 0;
	}
</style>
