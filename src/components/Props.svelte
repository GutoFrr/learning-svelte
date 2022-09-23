<script>
  import Info from './props/Info.svelte'
  import Nested from './props/Nested.svelte'

  const pkg = {
    name: 'svelte',
    version: 3,
    speed: 'blazing',
    website: 'https://svelte.dev',
  }
</script>

<Nested answer={42} />
<Info {...pkg} />
