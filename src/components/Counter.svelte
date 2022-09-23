<script>
  let count = 0
  $: doubled = count * 2

  const incrementCount = () => {
    count += 1
  }

  const resetCount = () => {
    count = 0
  }
</script>

<main>
  <h2 class="title">Counter</h2>
  <button on:click={incrementCount} class="btn">
    count is {count}
  </button>
  <button on:click={resetCount} class="btn"> reset count </button>

  <p>{count} doubled is {doubled}</p>
</main>
