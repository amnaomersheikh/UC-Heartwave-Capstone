
  <Button color="secondary" on:click={() => clicked++} variant="raised">
	<Label>Raised</Label>
  </Button>
  

  <script lang="ts">
	import Button, { Label } from '@smui/button';
  
	let clicked = 0;
  </script>