<script>
  let count = 0;

  // $: console.log('the count is ' + count);
  $: {
    console.log('the count is ' + count);
    // alert('I said count is ' + count)
  }
  function handleClick() {
    count += 1;
  }
</script>

<div>
  <h1>02-3. Statements</h1>
  <p>반응형의 경우 임의의 코드 문장으로 실행시킬 수도 있다.</p>
  <button on:click={handleClick}>
    Clicked {count} {count === 1 ? 'time' : 'times'}
  </button>
</div>