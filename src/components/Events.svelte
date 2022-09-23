<script>
  import ComponentEvents from './events/ComponentEvents.svelte'
  import DomEvents from './events/DOMEvents.svelte'
  import EventModifiers from './events/EventModifiers.svelte'

  const handleMessage = (event) => {
    alert(event.detail.text)
  }
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
  <div>
    <h2 class="section-title">Component Events</h2>
    <ComponentEvents on:message={handleMessage} />
  </div>
</main>
