<script>
	import YoutubeVideo from '$lib/YoutubeVideo.svelte';
	import { onMount } from 'svelte';

	onMount(() => {
		document.body.style.overflowY = 'visible';
	});

	const videos = [
		{
			title: 'NAHABA - GLASS',
			src: 'https://www.youtube.com/embed/iAP62Ffu3UA?si=ZBmwUD48Va4vAYQR'
		},
		{
			title: 'NAHABA - РІЖУ',
			src: 'https://www.youtube.com/embed/2P9H5aCBk40?si=Pa2TIcQURQt6N-O'
		},
		{
			title: 'NAHABA - 209 (feat. Milnyk)',
			src: 'https://www.youtube.com/embed/BecgjA6oBes?si=bvr5DnzE5-REFBs7'
		},
		{
			title: "NAHABA - WID'MA",
			src: 'https://www.youtube.com/embed/YGTZ1kTQHHs?si=mg9IERd7-ZFljinP'
		},
		{
			title: 'NAHABA - VESNIANKA',
			src: 'https://www.youtube.com/embed/bKxMirN_poA?si=A2VO-d-Iqs5xacBU'
		}
	];
</script>

<svelte:head>
	<title>Відео</title>
	<meta name="description" content="Подивись і послухай нахаб" />
</svelte:head>

<section>
	{#each videos as { title, src }}
		<YoutubeVideo {title} {src} />
	{/each}
</section>

<style>
	section {
		display: flex;
		align-items: center;
		flex-direction: column;
		gap: 32px;
		width: 100%;
		padding-bottom: 64px;

		@media (min-width: 700px) {
			gap: 128px;
		}
	}
</style>
