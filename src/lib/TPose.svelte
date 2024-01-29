<script lang="ts">
	export let src: string;
	export let character: 'A' | 'O';
</script>

<div>
	<a href={`/game?character=${character}`}>
		<img {src} alt="tpose character link" />
	</a>
</div>

<style>
	a {
		cursor: pointer;
	}
	img {
		width: 110px;

		@media (min-width: 700px) {
			width: 150px;
		}
	}
</style>
