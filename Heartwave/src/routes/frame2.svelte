<script context="module">
	export const prerender = true;
</script>

<script>
	import Counter from '$lib/Counter.svelte';

</script>

<svelte:head>
	<title>Frame 2</title>
</svelte:head>

<section>
	<h1>
		<div class="welcome">
			<picture>
				<img src="ucheartwave.png" alt="Welcome" />
			</picture>
		</div>

		to your new<br />frame 2
	</h1>

	<h2>
		try editing <strong>src/routes/index.svelte</strong>
	
	</h2>


</section>

<style>
	section {
		display: flex;
		flex-direction: column;
		justify-content: center;
		align-items: center;
		flex: 1;
	}

	h1 {
		width: 100%;
	}


</style>
