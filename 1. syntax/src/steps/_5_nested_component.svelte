<script>
  // 1. We can use keyword import
  // Notes: Any name will do, does not need to follow file name
  import HelloWorld from './_1_basics.svelte';

  let name = "Rain Chai";

  let image = "https://svelte.dev/tutorial/image.gif";
  let image_alt = "A man dancing";
</script>

<h1 class="hello">Hello {name}!</h1>
<img src={image} alt={image_alt} />
<!-- 2. Use it as a HTML tag! -->
<HelloWorld/>

<style>
  .hello {
    color: blue;
  }
</style>
