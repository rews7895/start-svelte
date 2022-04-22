<script>
	let w;
	let h;
	let size = 42;
	let text = 'edit me';
</script>

<div>
  <h1>06-11. Dimensions</h1>
  <p>모든 블록 수준 요소에는 clientWidth, clientHeight, offsetWidth, offsetHeight와 같은 것들을 사용할 수 있다.</p>
</div>
<input type=range bind:value={size}>
<input bind:value={text}>

<p>size: {w}px x {h}px</p>

<div bind:clientWidth={w} bind:clientHeight={h}>
	<span style="font-size: {size}px">{text}</span>
</div>

<style>
	input { display: block; }
	div { display: inline-block;}
	span { word-break: break-all; }
</style>