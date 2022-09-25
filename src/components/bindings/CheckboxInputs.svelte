<script>
  let yes = false
</script>

<label>
  <input type="checkbox" bind:checked={yes} />
  Yes! Send me regular email spam
</label>

{#if yes}
  <p>Thank you. We weill bombard your inbox and sell your personal details.</p>
{:else}
  <p>You must opt in to continue. If you're not paying, you're the product.</p>
{/if}

<button disabled={!yes} class={yes ? 'btn' : 'btn brightness-75 hover:brightness-75'}> Subscribe </button>
