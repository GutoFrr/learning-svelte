<script>
  let w
  let h
  let size = 42
  let text = 'edit me'
</script>

<main class="flex flex-col gap-1">
  <input type="range" bind:value={size} />
  <input bind:value={text} class="border-2 border-svelte py-1 px-2 rounded" />

  <p>size: {w}px x {h}px</p>

  <div bind:clientWidth={w} bind:clientHeight={h}>
    <span style="font-size: {size}px">{text}</span>
  </div>
</main>
