<script context="module">
	export const prerender = true;
</script>

<script>
	import Button from '$lib/Button.svelte';
	import Radio from '$lib/radio.svelte';
	let files;
</script>


<svelte:head>
	<title>First Frame</title>
</svelte:head>



<section>

	
	<h1>
		<div class="welcome">
			<picture>
				<img src="ucheartwave.png" alt="Welcome" />
			</picture>
		</div>
		<br/>
	
	</h1>
	<Radio/> 
	<h2>
		<div>
			<b>Start by uploading an ECG file...</b>
		</div>
		<br/>
		<br/>
	</h2>
	
	<input type="file" bind:files >

	{#if files && files[0]}
	<p>
		{files[0].name}
	</p>
	{/if}

	<Button/>

	<h2>
		<br/>
		<br/>
		<br/>
		<div>
			<b>Instructions: </b> 
		</div>
		
		<ul style="list-style-tyoe:dics">
			<li>Select ECG data file (CSV format)</li> 
			<li>Click 'Analyse' button</li>
		</ul>
		
		<br/>
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


