<!-- 2. Declare a script tag -->
<script>
  // 3. Declare counter variable
  let counter = 0;
  // 4. Declare an increment function
  function increment() {
    counter += 1;
  }
</script>

<!-- 1. Create a button! -->
<button puttingItAsAComment="5. Add a on:click attribute" on:click={increment}>Click me</button>

<!-- 6. Add p tag and reference variable! -->
<p>{counter}</p>
