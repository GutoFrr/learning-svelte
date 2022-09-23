<script>
  import Thing from './Thing.svelte'

  let things = [
    { id: 1, name: 'apple' },
    { id: 2, name: 'banana' },
    { id: 3, name: 'carrot' },
    { id: 4, name: 'doughnut' },
    { id: 5, name: 'egg' },
  ]

  const handleClick = () => {
    things = things.slice(1)
  }

  const resetThings = () => {
    things = [
      { id: 1, name: 'apple' },
      { id: 2, name: 'banana' },
      { id: 3, name: 'carrot' },
      { id: 4, name: 'doughnut' },
      { id: 5, name: 'egg' },
    ]
  }
</script>

{#if things.length > 0}
  <button on:click={handleClick} class="btn"> Remove first thing </button>
{:else}
  <button on:click={resetThings} class="btn"> Reset things </button>
{/if}

{#each things as thing (thing.id)}
  <Thing name={thing.name} />
{/each}
