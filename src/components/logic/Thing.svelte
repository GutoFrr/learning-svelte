<script>
  const emojis = {
    apple: '🍎',
    banana: '🍌',
    carrot: '🥕',
    doughnut: '🍩',
    egg: '🥚',
  }

  // the name is updated whenever the prop value changes...
  export let name

  // ...but the "emoji" variable is fixed upon initialisation of the component
  const emoji = emojis[name]
</script>

<p class="my-3">
  <span class="inline-block py-1 px-4 text-center rounded-sm">
    The emoji for {name} is {emoji}
  </span>
</p>

<style>
  span {
    background-color: #ffdfd3;
  }
</style>
