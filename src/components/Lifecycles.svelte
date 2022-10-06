<script>
  import OnDestroy from './lifecycles/OnDestroy.svelte'
  import OnMount from './lifecycles/OnMount.svelte'
</script>

<main class="grid grid-cols-3">
  <div>
    <h2 class="section-title">onMount</h2>
    <OnMount />
  </div>
  <div>
    <h2 class="section-title">onDestroy</h2>
    <OnDestroy />
  </div>
</main>
