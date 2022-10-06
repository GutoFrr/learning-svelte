<script>
  // @ts-nocheck

  import Timer from './Timer.svelte'

  let open = true
  let seconds = 0

  const toggle = () => (open = !open)
  const handleTick = () => (seconds += 1)
</script>

<div class="w-auto">
  <button on:click={toggle} class="btn">{open ? 'Close' : 'Open'} Timer</button>
  <p>
    The Timer component has been open for {seconds}
    {seconds === 1 ? 'second' : 'seconds'}
  </p>
  {#if open}
    <Timer callback={handleTick} />
  {/if}
</div>
