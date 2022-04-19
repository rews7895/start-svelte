<script>
  let count = 0;

  function incrementCount() {
    count += 1;
  }
</script>

<div>
  <h1>02-1. Assignments</h1>
  <p>이벤트에 대한 응답과 같이 DOM을 애플리케이션 상태와 동기화하기 위한 강력한 반응성 시스템이 존재</p>
  <p>이벤트 핸들러를 연결해야한다.</p>
  <button on:click={incrementCount}>
    Clicked {count} {count === 1 ? 'time' : 'times'}
  </button>
</div>