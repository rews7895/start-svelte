<script>
	import { marked } from 'marked';

	let value = `Some words are *italic*, some are **bold**`;
</script>

<div>
  <h1>06-5. Textarea Inputs</h1>
  <p>textarea도 마찬가지로 bind를 사용할 수 있다.</p>

  {@html marked(value)}

  <!-- <textarea bind:value={value}></textarea> -->
  <textarea bind:value></textarea>
</div>

<style>
	textarea { width: 100%; height: 200px; }
</style>