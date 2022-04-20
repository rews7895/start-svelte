<script>
	let m = { x: 0, y: 0 };

	function handleMousemove(event) {
		m.x = event.clientX;
		m.y = event.clientY;
	}
</script>

<div>
  <h1>05-1. Dom Events</h1>
  <p>on: 지시문을 사용하여 모든 이벤트를 수신할 수 있다.</p>
  <div class="move-area" on:mousemove={handleMousemove}>
    The mouse position is {m.x} x {m.y}
  </div>
</div>

<style>
	.move-area { width: 50%; height: 10em; background-color: azure;}
</style>