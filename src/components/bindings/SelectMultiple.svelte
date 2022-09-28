<script>
  let scoops = 1
  let flavours = ['Mint choc chip']

  let menu = ['Cookies and cream', 'Mint choc chip', 'Raspberry ripple']

  const join = (flavours) => {
    if (flavours.length === 1) return flavours[0]
    return `${flavours.slice(0, -1).join(', ')} and ${
      flavours[flavours.length - 1]
    }`
  }
</script>

<section class="flex flex-col gap-1 mb-3">
  <h3 class="text-xl mb-2">Size</h3>
  <label>
    <input type="radio" bind:group={scoops} name="scoops" value={1} />
    One scoop
  </label>
  <label>
    <input type="radio" bind:group={scoops} name="scoops" value={2} />
    Two scoop
  </label>
  <label>
    <input type="radio" bind:group={scoops} name="scoops" value={3} />
    Three scoop
  </label>
</section>

<select multiple bind:value={flavours} class="flex flex-col gap-1 mb-1 border-2 border-svelte">
  {#each menu as flavour}
    <option value={flavour}>
      {flavour}
    </option>
  {/each}
</select>

{#if flavours.length === 0}
  <p>Please select at least one flavour</p>
{:else if flavours.length > scoops}
  <p>Can't order more flavours than scoops!</p>
{:else}
  <p>
    You ordered {scoops}
    {scoops === 1 ? 'scoop' : 'scoops'} of {join(flavours)}
  </p>
{/if}
