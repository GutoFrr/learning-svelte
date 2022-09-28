<script>
  import InputField from './InputField.svelte'

  let field
</script>

<InputField bind:this={field} />
<button on:click={() => field.focus()} class="btn">focus field</button>
