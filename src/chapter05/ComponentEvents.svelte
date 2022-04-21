<script>
	import Inner from './ComponentEvents/Inner.svelte';

	function handleMessage(event) {
		alert(event.detail.text);
	}
</script>

<div>
  <h1>05-4. Component Events</h1>
  <p>구성요소는 이벤트를 전달할 수도 있다.</p>
  <p>이벤트를 전달하려면 dispatcher를 만들어야한다.</p>
  <p>컴포넌트는 이벤트를 수신할 속성을 추가해줘야 한다. on: message</p>
  <p>만약 수신할 속성이 없을 경우 메세지에 계속 발송되지만, 이에 반응하지 않는다.</p>
  <Inner on:message={handleMessage}/>
</div>