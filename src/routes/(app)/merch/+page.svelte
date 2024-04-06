<script>
	import comingSoonJPG from '$lib/assets/coming-soon.jpeg';
</script>

<section>
	<div>
		<p>Камінг сун</p>
		<img src={comingSoonJPG} alt="coming soon" />
	</div>
</section>

<style>
	p {
		font-family: 'Comic Sans MS', cursive;
		text-align: center;
		font-size: 20px;
		position: absolute;
		transform: translate(-50%, -50%);
		top: 50%;
		left: 50%;
	}
	img {
		max-height: 35vw;
		width: 90vw;
	}
	div {
		position: relative;
		display: flex;
		color: white;
		flex-direction: column;
	}
</style>
