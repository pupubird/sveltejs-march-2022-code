<script>
  const emojis = {
    apple: "🍎",
    banana: "🍌",
    carrot: "🥕",
    donute: "🍩",
  };

  // the name is updated whenever the prop value changes...
  export let fruit;

  // ...but the "emoji" variable is fixed upon initialisation of the component
  const emoji = emojis[fruit];
</script>

<p>
  {emoji}
  {fruit}
</p>
