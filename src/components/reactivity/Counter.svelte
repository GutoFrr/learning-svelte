<script>
  let count = 0
  // this declaration "$" keeps variables in sync with each other.
  $: doubled = count * 2

  const incrementCount = () => {
    count += 1
  }

  // you can also run statements reactively.
  $: {
    console.log(`the count is ${count}`)
  }

  $: if (count >= 10) {
    alert('count is dangerously high!')
    count = 9
    resetCount()
  }

  const resetCount = () => {
    count = 0
    console.clear()
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
