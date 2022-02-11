<script lang="ts">
import CustomInput from "$lib/CustomInput.svelte";

let valueArray = [];

const addInput = () => {
  valueArray = [...valueArray, {}]
};

const removeElement = (index: number) => {
  valueArray = valueArray.filter((_, i) => i !== index);
};

</script>
<div class="space-y-2">
  {#each valueArray as singleValue, i}
    <CustomInput on:remove={() => removeElement(i)} bind:value={singleValue}/>
  {/each}
  <button class="bg-blue-500 p-2 rounded-lg text-white" on:click={addInput}>✚ Add input</button>
</div>




{JSON.stringify(valueArray)}
