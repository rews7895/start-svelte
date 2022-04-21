<script>
	import Outer from "./EventForwarding/Outer.svelte";

	function handleMessage(event) {
		alert(event.detail.text);
	}
</script>

<div>
  <h1>05-5. Event Forwarding</h1>
  <p>DOM 이벤트와 달리 컴포넌트 이벤트는 버블링되지 않는다.</p>
  <p>일부 깊게 중첩된 컴포넌트에서 이벤트를 수신하려면 중간 컴포넌트가 이벤트를 전달해줘야한다.</p>
  <p>전달할 때는 중간 컴포넌트에 약칭으로 on:속성명을 사용</p>
  
  <Outer on:message={handleMessage}/>
</div>