<script>
  let isLoggedIn = false;

  function login() {
    isLoggedIn = true;
  }

  function logout() {
    isLoggedIn = false;
  }
</script>

<button on:click={login}>Log In</button>
<button on:click={logout}>Log Out</button>

<!-- 1. Convert to else -->
{#if isLoggedIn}
  <p>Logged In</p>
{:else}
  <p>Logged Out</p>
{/if}
