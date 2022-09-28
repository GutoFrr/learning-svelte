<script>
  import Keypad from './Keypad.svelte'

  let pin

  $: view = pin ? pin.replace(/\d(?!$)/g, '•') : 'enter your pin'

  const handleSubmit = () => {
    alert(`submitted ${pin}`)
  }
</script>

<h3 class="text-xl {pin ? 'text-black' : 'text-gray-400'}">{view}</h3>

<Keypad bind:value={pin} on:submit={handleSubmit} />
