<script>
  let name = 'gustavo'
</script>

<input
  bind:value={name}
  class="border-2 rounded px-2 py-1 border-svelte mb-2 outline-none"
/>

<h3 class="text-lg font-medium">
  Hello <span class="text-svelte">{name}!</span>
</h3>
