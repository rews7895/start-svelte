<script>
  let x = 7;
</script>

<div>
  <h1>04-3. Else if</h1>
  <p>여러 조건을 연결할 때는 else if를 사용한다.</p>
  {#if x > 10}
    <p>{x} is greater than 10</p>
  {:else if 5 > x}
    <p>{x} is less than 5</p>
  {:else}
    <p>{x} is between 5 and 10</p>
  {/if}
</div>