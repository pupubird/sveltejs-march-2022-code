<!-- 1. Add script -->
<script>
  // 2. Add fetch
  let number = fetch("https://svelte.dev/tutorial/random-number")
    .then((p) => p.text())
    .then((v) => v);
</script>

<!-- 3. We want to show "Loading" when it's fetching, hence we can use await -->
{#await number}
  <p>Loading...</p>
  <!-- When promise is resolved -->
{:then value}
  <p>Value: {value}</p>
{/await}
