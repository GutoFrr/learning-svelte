<script>
  import { onInterval } from './utils.js'

  export let callback
  export let interval = 1000

  onInterval(callback, interval)
</script>

<p class="border-2 border-blue-500 p-1">
  This component executes a callback every {interval} 
  millisecond{interval === 1 ? '' : 's'}
</p>

