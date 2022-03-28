<script>
  // 1. Declare an array
  let history = [];
  let counter = 0;
  let doubled = 0;
  function increment() {
    counter += 1;
  }
  $: doubled = counter * 2;
  // 2. Create a new statement
  // NOTES: this will listen to "doubled"
  $: {
    // This will not work.
    // history.push(doubled);

    // This will work
    history = [...history, doubled];
    console.log(history)
  }
</script>

<button on:click={increment}>Click me</button>
<p>{counter}</p>
<p>{doubled}</p>
<!-- 3. Create new tag -->
<p>{history}</p>