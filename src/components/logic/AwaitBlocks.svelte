<script>
  const getRandomNumber = async () => {
    const res = await fetch(`/tutorial/random-number`)
    const text = await res.text()

    if (res.ok) {
      return text
    } else {
      throw new Error(text)
    }
  }

  let promise = getRandomNumber()

  const handleClick = () => {
    promise = getRandomNumber()
  }
</script>

<button on:click={handleClick} class="btn"> generate random number </button>

{#await promise}
  <p>...waiting</p>
{:then number}
  <p>The number is {number}</p>
{:catch error}
  <p>{error.message}</p>
{/await}
