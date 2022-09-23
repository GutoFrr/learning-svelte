<script>
  let mouse = { x: 0, y: 0 }

  const handleMouseMove = (event) => {
    mouse.x = event.clientX
    mouse.y = event.clientY
  }
</script>

<div on:mousemove={handleMouseMove} class="w-72 h-60 border-2 border-svelte">
  The mouse position is {mouse.x} x {mouse.y}
</div>
