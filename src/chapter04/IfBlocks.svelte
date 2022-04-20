<script>
  let user = {loggedIn: false};

  function toggle() {
    user.loggedIn = !user.loggedIn;
  }
</script>

<div>
  <h1>04-1. If Blocks</h1>
  <p>조건부로 렌더링하기 위해 If를 사용</p>

  {#if user.loggedIn}
    <button on:click={toggle}>
      Log out
    </button>
  {/if}

  {#if !user.loggedIn}
    <button on:click={toggle}>
      Log in
    </button>
  {/if}
</div>

<style>
  button {width: 5em;}
</style>