<script>
  import BindingInstances from './bindings/BindingInstances.svelte'
  import CheckboxInputs from './bindings/CheckboxInputs.svelte'
  import ComponentBindings from './bindings/ComponentBindings.svelte'
  import ContentEditable from './bindings/ContentEditable.svelte'
  import Dimensions from './bindings/Dimensions.svelte'
  import EachBlockBindings from './bindings/EachBlockBindings.svelte'
  import GroupInputs from './bindings/GroupInputs.svelte'
  import NumericInputs from './bindings/NumericInputs.svelte'
  import Select from './bindings/Select.svelte'
  import SelectMultiple from './bindings/SelectMultiple.svelte'
  import TextareaInputs from './bindings/TextareaInputs.svelte'
  import TextInputs from './bindings/TextInputs.svelte'
</script>

<main class="grid grid-cols-3 gap-10">
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
  <div>
    <h2 class="section-title">Select Multiple</h2>
    <SelectMultiple />
  </div>
  <div>
    <h2 class="section-title">Contenteditable Bindings</h2>
    <ContentEditable />
  </div>
  <div>
    <h2 class="section-title">Each Block Bindings</h2>
    <EachBlockBindings />
  </div>
  <div>
    <h2 class="section-title">Dimensions</h2>
    <Dimensions />
  </div>
  <div>
    <h2 class="section-title">Component Bindings</h2>
    <ComponentBindings />
  </div>
  <div>
    <h2 class="section-title">Binding Instances</h2>
    <BindingInstances />
  </div>
</main>

<style>
  div {
    @apply border-2 border-svelte p-6;
  }
</style>
