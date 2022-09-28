<script>
  import { createEventDispatcher } from 'svelte'

  export let value = ''

  const dispatch = createEventDispatcher()

  const select = (num) => () => (value += num)
  const clear = () => (value = '')
  const submit = () => dispatch('submit')
</script>

<div class="grid grid-cols-3 grid-rows-4 gap-2">
  <button on:click={select(1)}>1</button>
  <button on:click={select(2)}>2</button>
  <button on:click={select(3)}>3</button>
  <button on:click={select(4)}>4</button>
  <button on:click={select(5)}>5</button>
  <button on:click={select(6)}>6</button>
  <button on:click={select(7)}>7</button>
  <button on:click={select(8)}>8</button>
  <button on:click={select(9)}>9</button>

  <button disabled={!value} on:click={clear}>clear</button>
  <button on:click={select(0)}>0</button>
  <button disabled={!value} on:click={submit} class="btn">submit</button>
</div>

<style>
  button {
    @apply bg-slate-400 py-2 px-4 w-20 rounded text-white cursor-pointer;
  }

  button:hover {
    @apply brightness-90;
  }

  .btn {
    @apply bg-svelte;
  }
</style>
