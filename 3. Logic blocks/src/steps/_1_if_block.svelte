<!-- 2. Add script tag -->
<script>
  // 3. Create loggedIn variable
  let isLoggedIn = false;
  // 4. Create log in function
  function login() {
    isLoggedIn = true;
  }
  // 5. Create log out function
  function logout() {
    isLoggedIn = false;
  }
</script>

<!-- 1. Create 2 buttons -->
<button on:click={login}>Log In</button>
<button on:click={logout}>Log Out</button>

<!-- 6. Add if tag -->
{#if isLoggedIn}
  <p>Logged In</p>
{/if}

<!-- 7. Add if tag -->

{#if !isLoggedIn}
  <p>Logged Out</p>
{/if}
