<script>
	let name = 'world';
</script>

<div>
  <h1>06-1. Text Inputs</h1>
  <p>bind를 사용하게 되면 입력 값을 변경할 수 있다</p>
  <input bind:value={name}>

  <h1>Hello {name}!</h1>
</div>