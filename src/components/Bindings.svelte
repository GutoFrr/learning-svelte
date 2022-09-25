<script>
  import NumericInputs from './bindings/NumericInputs.svelte'
  import TextInputs from './bindings/TextInputs.svelte'
</script>

<main class="flex flex-col gap-5">
  <div>
    <h2 class="section-title">Text Inputs</h2>
    <TextInputs />
  </div>
  <div>
    <h2 class="section-title">Numeric Inputs</h2>
    <NumericInputs />
  </div>
</main>
