<script>
  import { Router, Route, Link } from 'svelte-navigator'
  import Events from './components/Events.svelte'
  import Logic from './components/Logic.svelte'
  import Props from './components/Props.svelte'
  import Reactivity from './components/Reactivity.svelte'
</script>

<Router>
  <nav class="px-10 py-3 flex items-center gap-4">
    <h1 class="text-xl font-bold">Learning Svelte!</h1>
    <Link to="/">Home</Link>
    <Link to="reactivity">Reactivity</Link>
    <Link to="props">Props</Link>
    <Link to="logic">Logic</Link>
    <Link to="events">Events</Link>
  </nav>

  <main>
    <div class="px-10 py-3">
      <Route>
        <h1 class="title">
          Hello World by <span class="text-svelte">Svelte!</span>
        </h1>
      </Route>

      <Route path="reactivity">
        <h1 class="title">Reactivity</h1>
        <Reactivity />
      </Route>

      <Route path="props">
        <h1 class="title">Props</h1>
        <Props />
      </Route>

      <Route path="logic">
        <h1 class="title">Logic</h1>
        <Logic />
      </Route>

      <Route path="events">
        <h1 class="title">Events</h1>
        <Events />
      </Route>
    </div>
  </main>
</Router>

<style>
</style>
