<script context="module">
	export const prerender = true;
</script>

<script>
	import Button from '$lib/Button.svelte';
	let files;
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

	<label>Press 'browse' and select file</label>
	<input type="file" bind:files >

	{#if files && files[0]}
	<p>
		{files[0].name}
	</p>
	{/if}
	<Button/>
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
