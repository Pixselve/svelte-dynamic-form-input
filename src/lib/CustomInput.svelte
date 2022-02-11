<div class="flex space-x-2">
  <select  class="bg-blue-100 rounded-lg p-2 border border-blue-300 appearance-none after:content-['-'] after:absolute after:top-2 after:right-0" bind:value={value.dropdown}>
    <option value="🐶">🐶</option>
    <option value="🐱">🐱</option>
    <option value="🐭">🐭</option>
  </select>
  <input class="bg-blue-100 rounded-lg p-2 border border-blue-300" bind:value={value.input} placeholder="Type here..." type="text">
  <button on:click={remove}>❌</button>
</div>

<script lang="ts">
import { createEventDispatcher } from "svelte";

const dispatch = createEventDispatcher();
const remove = () => dispatch('remove');
export let value = {
  dropdown: "🐶",
  input: ""
}
</script>
