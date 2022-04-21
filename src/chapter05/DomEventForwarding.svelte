<script>
	import CustomButton from './DomEventForwarding/Inner.svelte';

	function handleClick() {
		alert('Button Clicked');
	}
</script>

<div>
  <h1>05-6. Dom Event Forwarding</h1>
  <p>이벤트 전달은 DOM 이벤트에서도 작동.</p>
  <p>클릭에 대한 이벤트를 전달하려면 on:click을 약식으로 붙여주면 된다.</p>
  <CustomButton on:click={handleClick}/>
</div>