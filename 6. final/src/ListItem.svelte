<script>
  export let title = "Todo item 1";
  export let createdAt = new Date();
  export let checked = false;
  export let onCheckboxChecked = () => {};
  $: {
    if (checked) {
      onCheckboxChecked();
    }
  }
</script>

<div class="row">
  <input
    type="checkbox"
    name="checkbox"
    id={title + createdAt.getUTCMilliseconds()}
    bind:checked
  />
  <label for={title + createdAt.getUTCMilliseconds()}>
    {#if checked}
      <del>
        <p>{title}</p>
        <p>{createdAt}</p>
      </del>
    {:else}
      <p>{title}</p>
      <p>{createdAt}</p>
    {/if}
  </label>
</div>

<style>
  .row {
    display: flex;
    align-items: center;
  }
  .row * {
    margin-right: 10px;
  }
  .row label,
  .row label del {
    display: flex;
  }
</style>
