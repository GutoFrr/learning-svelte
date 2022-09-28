<script>
  let todos = [
    { done: false, text: 'finish Svelte tutorial' },
    { done: false, text: 'build an app' },
    { done: false, text: 'world domination' },
  ]

  const add = () => {
    todos = todos.concat({ done: false, text: '' })
  }

  const clear = () => {
    todos = todos.filter((todo) => !todo.done)
  }

  $: remaining = todos.filter((todo) => todo.done).length
</script>

<main>
  <h3 class="text-xl mb-2">Todos</h3>
  <div class="flex flex-col gap-2">
    {#each todos as todo}
      <div class:opacity-40={todo.done} class="p-1.5">
        <input type="checkbox" bind:checked={todo.done} />

        <input
          placeholder="What needs to be done?"
          bind:value={todo.text}
          class="border-2 border-svelte rounded p-1"
        />
      </div>
    {/each}
  </div>
  <p>{remaining} remaining</p>
  <button on:click={add} class="btn"> add new </button>
  <button on:click={clear} class="btn">clear completed</button>
</main>

<style>
</style>
