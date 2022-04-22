<script>
	import Keypad from './ComponentBindings/Keypad.svelte';

	let pin;
	$: view = pin ? pin.replace(/\d(?!$)/g, '•') : 'enter your pin';

	function handleSubmit() {
		alert(`submitted ${pin}`);
	}
</script>

<div>
  <h1>06-13. Component Binding</h1>
  <p>컴포넌트를 바인딩 할 수도 있다.</p>
  <h1 style="color: {pin ? '#333' : '#ccc'}">{view}</h1>

  <Keypad bind:value={pin} on:submit={handleSubmit}/>
</div>
