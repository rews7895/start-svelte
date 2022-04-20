<script>
  let user = {loggedIn: false};

  function toggle() {
    user.loggedIn = !user.loggedIn;
  }
</script>

<div>
  <h1>04-2. Else Blocks</h1>
  <p>상호 배타적으로 사용할때는 if ~ else를 사용한다.</p>
  <p>참고로 열기태그( # ) / 연속태그( : ) / 닫기태그( / ) 이다 </p>
  {#if user.loggedIn}
    <button on:click={toggle}>
      Log out
    </button>
  {:else}
    <button on:click={toggle}>
      Log in
    </button>
  {/if}
</div>

<style>
  button {width: 5em;}
</style>