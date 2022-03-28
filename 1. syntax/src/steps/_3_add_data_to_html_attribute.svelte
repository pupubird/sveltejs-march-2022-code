<script>
  let name = "Rain Chai";
  // 1. Declare a new variable!
  let image = "https://svelte.dev/tutorial/image.gif";
  let image_alt = "A man dancing";
</script>

<h1>Hello {name}!</h1>
<!-- 2. Add image url to image, use { } to reference -->
<img src={image} alt={image_alt} />
