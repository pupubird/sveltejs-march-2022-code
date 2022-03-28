<!-- 1. Import -->
<script>
    import Button from "./button.svelte";

    // 2. Create function
    function onTimeout(e){
        // e.detail is the second parameter from dispatch()
        alert(e.detail)
    }
</script>

<!-- 3. on: directive to catch the event -->
<Button on:timeout={onTimeout}/>