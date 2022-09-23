<script>
  // @ts-ignore
  import AddANumber from './reactivity/AddANumber.svelte'
  import Counter from './reactivity/Counter.svelte'
</script>

<main class="flex flex-col gap-5">
  <div>
    <h2 class="section-title">Counter</h2>
    <Counter />
  </div>
  <div>
    <h2 class="section-title">Updating Array Dynamically</h2>
    <AddANumber />
  </div>
</main>
