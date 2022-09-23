<script>
  import EachBlocks from './logic/EachBlocks.svelte'
  import ElseIfBlocks from './logic/ElseIfBlocks.svelte'
  import IfBlock from './logic/IfBlocks.svelte'
  import KeyedEachBlocks from './logic/KeyedEachBlocks.svelte'
</script>

<main class="flex flex-col gap-5">
  <div>
    <h2 class="section-title">If Statement blocks</h2>
    <IfBlock />
  </div>
  <div>
    <h2 class="section-title">Else If Statement blocks</h2>
    <ElseIfBlocks />
  </div>
  <div>
    <h2 class="section-title">Each blocks</h2>
    <EachBlocks />
  </div>
  <div>
    <h2 class="section-title">Keyed Each blocks</h2>
    <KeyedEachBlocks />
  </div>
</main>
