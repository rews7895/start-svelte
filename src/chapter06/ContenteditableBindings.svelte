<script>
	let html = '<p>Write some text!</p>';
</script>

<div>
  <h1>06-8. Contenteditable Bindings</h1>
  <p>div나 다른 요소를 input이나 textarea같이 편집하고 싶을 때 contenteditable=true하면 수정할 수 있다.</p>
  <div contenteditable="true" bind:innerHTML={html}></div>

  <pre>{html}</pre>
</div>

<style>
	[contenteditable] {
		padding: 0.5em;
		border: 1px solid #eee;
		border-radius: 4px;
	}
</style>