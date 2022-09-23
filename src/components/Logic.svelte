<script>
  import EachBlocks from './logic/EachBlocks.svelte'
  import ElseIfBlocks from './logic/ElseIfBlocks.svelte'
  import IfBlock from './logic/IfBlocks.svelte'
</script>

<main class="flex flex-col gap-5">
  <div>
    <h2 class="section-title">If Statement block</h2>
    <IfBlock />
  </div>
  <div>
    <h2 class="section-title">Else If Statement block</h2>
    <ElseIfBlocks />
  </div>
  <div>
    <h2 class="section-title">Each block</h2>
    <EachBlocks />
  </div>
</main>
