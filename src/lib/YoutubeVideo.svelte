<script lang="ts">
	export let src: string;
	export let title: string;
</script>

<div class="video-container">
	<iframe
		{src}
		{title}
		height="100%"
		width="100%"
		frameborder="0"
		allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share"
		allowfullscreen
	></iframe>
</div>

<style>
	.video-container {
		width: 100%;
		aspect-ratio: 16/9;
		padding-bottom: 64px;

		@media (min-width: 1000px) {
			width: 70%;
		}
		@media (min-width: 1600px) {
			width: 60%;
		}
	}
</style>
