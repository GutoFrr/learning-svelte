<script>
  // @ts-nocheck

  import { marked } from 'marked'
  let value = `Some words are *italic*, some are **bold**`
</script>

{@html marked(value)}

<textarea {value} class="border-2 border-svelte w-60 resize-none outline-none rounded" />
