<script>
  let questions = [
    { id: 1, text: `Where did you go to school?` },
    { id: 2, text: `What is your mother's name?` },
    {
      id: 3,
      text: `What is another personal fact that an attacker could easily find with Google?`,
    },
  ]

  let selected

  let answer = ''

  const handleSubmit = () => {
    alert(
      `answered question ${selected.id} (${selected.text}) with "${answer}" `
    )
  }
</script>

<h3 class="text-xl mb-2">Insecurity questions</h3>

<form on:submit|preventDefault={handleSubmit} class="flex flex-col gap-2 w-96">
  <select
    bind:value={selected}
    on:change={() => (answer = '')}
    class="border-2 border-svelte outline-none rounded"
  >
    {#each questions as question}
      <option value={question}>
        {question.text}
      </option>
    {/each}
  </select>

  <input bind:value={answer} placeholder="answer..." class="border-2 border-svelte outline-none rounded py-1 px-2" />

  <button disabled={!answer} type="submit" class="btn w-32 mb-2">submit</button>
</form>

<p>selected question {selected ? selected.id : '[waiting...]'}</p>
