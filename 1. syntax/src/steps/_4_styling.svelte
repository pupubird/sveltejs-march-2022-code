<script>
  let name = "Rain Chai";

  let image = "https://svelte.dev/tutorial/image.gif";
  let image_alt = "A man dancing";
</script>

<!-- 2. Add class name to h1 tag -->
<h1 class="hello">Hello {name}!</h1>
<img src={image} alt={image_alt} />

<!-- 1. Declare style tag! -->
<style>
  .hello {
    color: blue;
  }
</style>

<!-- 3. Check out public/global.css! -->