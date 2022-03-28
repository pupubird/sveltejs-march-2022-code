<!-- 2. Add script -->
<script>
  // 3. Import function
  import { createEventDispatcher } from "svelte";
  // 4. Initialize function
  const dispatch = createEventDispatcher();

  // 5. Create fucntion
  function onClick() {
    // 6. Create timeout
    setTimeout(() => {
      dispatch("timeout", 'done!');
    }, 1000);
  }
</script>

<!-- 1. Add button -->
<button on:click={onClick}>Click me</button>
