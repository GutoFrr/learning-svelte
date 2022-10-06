<script>
  import { onMount } from 'svelte'

  let photos = []

  onMount(async () => {
    const res = await fetch(`/tutorial/api/album`)
    photos = await res.json()
  })
</script>

<h1 class="text-xl font-bold">Photo Album</h1>

<div class="grid grid-cols-5 gap-2">
  {#each photos as photo}
    <figure class="w-full m-0">
      <img src={photo.thumbnailUrl} alt={photo.title} class="w-full m-0" />
      <figcaption>{photo.title}</figcaption>
    </figure>
  {:else}
    <p>loading...</p>
  {/each}
</div>
