<div class="radio-demo">
  {#each options as option}
    <FormField>
      <Radio
        bind:group={selected}
        value={option.name}
        disabled={option.disabled}
      />
      <span slot="label">
        {option.name}{option.disabled ? ' (disabled)' : ''}
      </span>
    </FormField>
  {/each}
</div>

<div style="margin-top: 1em;">
  <Button
    on:click={() => {
      selected = 'Doc';
    }}
  >
    Select User Type
  </Button>
</div>

<pre class="status">Selected: {selected}</pre>

<script lang="ts">
  import Radio from '@smui/radio';
  import FormField from '@smui/form-field';
  import Button from '@smui/button';

  let options = [
    {
      name: 'General',
      disabled: false,
    },
    {
      name: 'Advanced',
      disabled: false,
    },
    
  ];
  let selected = 'General';
</script>

<style>
  .radio-demo > :global(*) {
    margin: 0 0.2em;
  }
  input[type="radio"]{
    width: 500px;
  }
  
</style>