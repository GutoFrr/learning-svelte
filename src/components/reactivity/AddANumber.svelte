<script>
  let numbers = [1, 2, 3, 4]

  const addNumber = () => {
    numbers = [...numbers, numbers.length + 1]
  }

  $: sum = numbers.reduce((t, n) => t + n, 0)

  const resetCount = () => {
    numbers = [1, 2, 3, 4]
  }

  $: if (numbers.length >= 10) {
    alert('count is dangerously high!')
    resetCount()
    sum = numbers.reduce((t, n) => t + n, 0)
  }
</script>

<main>
  <p>{numbers.join(' + ')} = {sum}</p>
  <button on:click={addNumber} class="btn"> add a number </button>
  <button on:click={resetCount} class="btn"> reset count </button>
</main>
