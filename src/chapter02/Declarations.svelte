<script>
  let count = 0;
  $: doubled = count * 2;

  function handleClick() {
    count += 1;
  }
</script>

<div>
  <h1>02-2. Declarations</h1>
  <p>Svelte는 구성요소의 상태가 변경되면 DOM을 자동으로 업데이트 한다.</p>
  <p>부가적으로 구성요소의 일부가 다른 부분에서 계산되어야 하고 변경이 필요할 때 반응형 선언을 사용한다.</p>
  <p>즉 참조해야할 값이 바뀌었을 때 다시 실행</p>
  <p>반응형 선언은 여러번 참조해야하거나 다른 반응 값에 의존하는 값이 있을 때 특히 유용.</p>
  <button on:click={handleClick}>
    Clicked {count} {count === 1 ? 'time' : 'times'}
  </button>
  <p>{count} doubled is {doubled}</p>
</div>