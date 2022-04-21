<script>
	let a = 1;
	let b = 2;
</script>

<div>
  <h1>06-2. Numeric Inputs</h1>
  <p>bind는 number나 range와 같은 숫자 관련해서도 값을 변경할 수 있다.</p>
  <label>
    <input type=number bind:value={a} min=0 max=10>
    <input type=range bind:value={a} min=0 max=10>
  </label>
  
  <label>
    <input type=number bind:value={b} min=0 max=10>
    <input type=range bind:value={b} min=0 max=10>
  </label>
  
  <p>{a} + {b} = {a + b}</p>  
</div>

<style>
	label { display: flex }
	input, p { margin: 6px }
</style>