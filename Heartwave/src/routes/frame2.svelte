<script context="module">
	export const prerender = true;
</script>

<script>
	import Button from '$lib/Button.svelte';
	
	let files;

	import Radio from '$lib/Radio2.svelte'
	
	let radioValue;
	
	const options = [{
		value: 'General',
		label: 'General',
	}, {
		value: 'Advanced',
		label: 'Advanced',
	}]
</script>


<svelte:head>
	<title>First Frame</title>
</svelte:head>



<section>
	<h1>
		<div style="display: flex; justify-content: space-around">
			<div >
				<picture>
					<img src="ucheartwave.png" alt="Welcome" />
				</picture>
			</div>
			<div>		
				<Radio {options} fontSize={16} legend='Select User Type' bind:userSelected={radioValue}/>
			</div>
		</div>
		<br/>
	</h1>

	<div  style="display: flex; justify-content: space-around; width:1500px">
		<div >
			<h2>
				<div>
					<b>Start by uploading an ECG file...</b>
					<br/>
					<br/>
					<br/>
				</div>
			</h2>
			
			<input type="file" bind:files >

			{#if files && files[0]}
			<p>
				{files[0].name}
			</p>
			{/if}
			<br>
			<br>
			<Button/>

			<h2>
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
		</div>
		<div>		
		
		</div>
	</div>

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


