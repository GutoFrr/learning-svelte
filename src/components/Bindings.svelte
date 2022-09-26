<script>
  import CheckboxInputs from './bindings/CheckboxInputs.svelte'
  import GroupInputs from './bindings/GroupInputs.svelte'
  import NumericInputs from './bindings/NumericInputs.svelte'
  import Select from './bindings/Select.svelte'
  import TextareaInputs from './bindings/TextareaInputs.svelte'
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
  <div>
    <h2 class="section-title">Checkbox Inputs</h2>
    <CheckboxInputs />
  </div>
  <div>
    <h2 class="section-title">Group Inputs</h2>
    <GroupInputs />
  </div>
  <div>
    <h2 class="section-title">Textarea Inputs</h2>
    <TextareaInputs />
  </div>
  <div>
    <h2 class="section-title">Select Bindings</h2>
    <Select />
  </div>
</main>
