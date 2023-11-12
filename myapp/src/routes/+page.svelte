<script>
  const arrayOfObjects = [
    {color: "red", type: "minivan", doorcount: "5", year: "2010"},
    {color: "green", type: "sedan", doorcount: "4", year: "2009"},
    {color: "blue", type: "truck", doorcount: "2", year: "2015"},
  ];
</script>

<h1>Welcome to SvelteKit</h1>
<p>Visit <a href="https://kit.svelte.dev">kit.svelte.dev</a> to read the documentation</p>

<label for="text-input">Text input</label>: 
<input type="text" id="text-input">

<!-- <script>
  import {arrayOfObjects} from '$lib/index.js';
</script> -->

<!-- function addObject() {
  let arrayOfObjects = {id: arrayOfObjects.length + 1, name: `Object ${arrayOfObjects.length + 1}`};
  arrayOfObjects = [...arrayOfObjects, newObject];
}; -->

<div>
  <h1>Array of Objects</h1>
  <ul>
    {#each arrayOfObjects as obj (obj.id)}
      <li>{obj.name}</li>
    {/each}
  </ul>

  <button on:click={addObject}>Add Object</button>
</div>