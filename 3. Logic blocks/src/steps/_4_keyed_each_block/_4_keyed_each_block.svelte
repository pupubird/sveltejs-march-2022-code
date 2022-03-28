<!-- Check https://svelte.dev/tutorial/keyed-each-blocks for full example -->
<script>
  import Item from "./item.svelte";
  let fruits = [
    { id: 1, fruit: "apple" },
    { id: 2, fruit: "banana" },
    { id: 3, fruit: "carrot" },
    { id: 4, fruit: "donute" },
  ];
  // 1. Add removeItem function
  function removeItem() {
    // To remove first item
    fruits = fruits.slice(1);
  }
</script>

<!-- 3. Add button -->
<button on:click={removeItem}>Remove first item</button>

<!-- 4. Add key -->
{#each fruits as item (item.id)}
  <div>
    <Item fruit={item.fruit} />
  </div>
{/each}
