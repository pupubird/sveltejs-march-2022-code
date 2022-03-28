<script>
  import ListItem from "./ListItem.svelte";
  let items = [];
  let title = "";
  function addItem() {
    items = [
      ...items,
      {
        id: items.length,
        title: title,
        createdAt: new Date(),
      },
    ];
    title = "";
  }

  function removeItemFromList(event) {
    let id = event.detail;
    let itemIndex = items.findIndex((i) => i.id == id);
    items.splice(itemIndex, 1);
    items = items;
  }
</script>

<div>
  <form on:submit|preventDefault>
    <input type="text" placeholder="Enter new task" bind:value={title} />
    <input type="submit" on:click={addItem} value="Add" />
  </form>
</div>

{#each items as item (item.id)}
  <ListItem {...item} on:checkboxChecked={removeItemFromList} />
{/each}
