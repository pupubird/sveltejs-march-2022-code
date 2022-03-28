<!-- 1. Add script tag -->
<script>
  // 2. Create array variable
  let history = [
    "https://google.com",
    "https://youtube.com",
    "https://svelte.dev",
  ];
</script>

<!-- 3. Add each block -->
{#each history as item}
  <p>{item}</p>
{/each}
