<script>
  let cats = [
    { id: 'J---aiyznGQ', name: 'Keyboard Cat' },
    { id: 'z_AbfPXTKms', name: 'Maru' },
    { id: 'OUtn3pvWmpg', name: 'Henri The Existential Cat' },
  ]
</script>

<h3 class="text-xl font-bold">The famous cats of Youtube</h3>
<ul>
  {#each cats as item}
    <li>
      <a target="_blank" href="https://www.youtube.com/watch?v={item.id}">
        {item.name}
      </a>
    </li>
  {/each}
</ul>
