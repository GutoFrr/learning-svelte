<script>
  let html = '<p>Write some text!</p>'
</script>

<div
  contenteditable="true"
  bind:innerHTML={html}
  class="border-2 border-svelte py-1 px-2 w-52 rounded"
/>

<pre>{html}</pre>
