<script>
  let count = 0
  // this declaration "$" keeps variables in sync with each other.
  $: doubled = count * 2

  const incrementCount = () => {
    count += 1
  }

  $: {
    console.log(`the count is ${count}`)
  }

  $: if (count >= 10) {
    alert('count is dangerously high!')
    count = 9
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
