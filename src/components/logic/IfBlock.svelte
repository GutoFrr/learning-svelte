<script>
  let user = { loggedIn: false }

  const toggleUser = () => {
    user.loggedIn = !user.loggedIn
  }
</script>

{#if user.loggedIn}
  <button on:click={toggleUser} class="btn"> Log out </button>
{/if}

{#if !user.loggedIn}
  <button on:click={toggleUser} class="btn"> Log in </button>
{/if}

<!-- with else statement
{#if user.loggedIn}
	<button on:click={toggle}>
		Log out
	</button>

{:else}
	<button on:click={toggle}>
		Log in
	</button>
{/if}
 -->
