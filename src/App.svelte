<script>
  import { Router, Route, Link } from 'svelte-navigator'
  import Reactivity from './components/Reactivity.svelte'
</script>

<Router>
  <nav class="px-10 py-3 flex items-center gap-4">
    <h1 class="text-xl font-bold">Learning Svelte!</h1>
    <Link to="/">Home</Link>
    <Link to="reactivity">Reactivity</Link>
    <Link to="props">Props</Link>
  </nav>

  <main>
    <div class="px-10 py-6">
      <Route>
        <h1 class="text-4xl font-bold">
          Hello World by <span class="text-svelte">Svelte!</span>
        </h1>
      </Route>

      <Route path="reactivity">
        <Reactivity />
      </Route>

      <Route path="props" />
    </div>
  </main>
</Router>

<style>
</style>
