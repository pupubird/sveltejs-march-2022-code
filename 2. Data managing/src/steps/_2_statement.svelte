<script>
  let counter = 0;
  // 1. Declare new variable
  let doubled = 0;
  function increment() {
    counter += 1;
  }
  // 2. Add it in the $:
  // NOTES: This will listen to "counter" variable, and update "doubled" when it changed
  $: doubled = counter * 2;

</script>

<button on:click={increment}>Click me</button>
<p>{counter}</p>
<!-- 3. Create new tag -->
<p>{doubled}</p>
