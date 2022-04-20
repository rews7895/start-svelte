<script>
  let m = { x: 0, y: 0 };

  // function handleMousemove(event) {
  //   m.x = event.clientX;
  //   m.y = event.clientY;
  // }
</script>

<div>
  <h1>05-2. Inline Handlers</h1>
  <p>이벤트 핸들러를 인라인으로 선언할 수도 있다.</p>

  <div class="move-area" on:mousemove={e => m = { x: e.clientX, y: e.clientY }}>
    The mouse position is {m.x} x {m.y}
  </div>
</div>

<style>
	.move-area { width: 50%; height: 10em; background-color: azure;}
</style>