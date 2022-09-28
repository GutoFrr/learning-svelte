<script>
  let input

  export const focus = () => {
    input.focus()
  }

</script>

<input bind:this={input} class="border-2 border-svelte rounded py-1.5 px-2" />
