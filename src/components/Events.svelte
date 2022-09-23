<script>
  import DomEvents from './events/DOMEvents.svelte'
  import EventModifiers from './events/EventModifiers.svelte'
</script>

<main class="flex flex-col gap-5">
  <div>
    <h2 class="section-title">DOM Events</h2>
    <DomEvents />
  </div>
  <div>
    <h2 class="section-title">Event Modifiers</h2>
    <EventModifiers />
  </div>
</main>
