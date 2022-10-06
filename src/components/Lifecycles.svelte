<script>
  import OnDestroy from './lifecycles/OnDestroy.svelte'
  import OnMount from './lifecycles/OnMount.svelte'
  import Tick from './lifecycles/Tick.svelte'
</script>

<main class="grid grid-cols-3 gap-10">
  <div>
    <h2 class="section-title">onMount</h2>
    <OnMount />
  </div>
  <div>
    <h2 class="section-title">onDestroy</h2>
    <OnDestroy />
  </div>
  <div>
    <h2 class="section-title">Tick</h2>
    <Tick />
  </div>
</main>
