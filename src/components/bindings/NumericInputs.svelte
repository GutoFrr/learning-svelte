<script>
  let a = 1
  let b = 2
  $: result = a + b
</script>

<label class="block mb-1">
  <input
    type="number"
    bind:value={a}
    min="0"
    max="10"
    class="border-svelte border-2 rounded p-1"
  />
  <input type="range" bind:value={a} min="0" max="10" />
</label>

<label>
  <input
    type="number"
    bind:value={b}
    min="0"
    max="10"
    class="border-svelte border-2 rounded p-1"
  />
  <input type="range" bind:value={b} min="0" max="10" />
</label>

<p>{a} + {b} = {result}</p>
