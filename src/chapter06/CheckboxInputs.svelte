<script>
	let yes = false;
</script>

<div>
  <h1>06-3. Checkbox Inputs</h1>
  <p>checkbox도 마찬가지 bind를 사용할 수 있다.</p>

  <label>
    <input type=checkbox bind:checked={yes}>
    Yes! Send me regular email spam
  </label>
  
  {#if yes}
    <p>Thank you. We will bombard your inbox and sell your personal details.</p>
  {:else}
    <p>You must opt in to continue. If you're not paying, you're the product.</p>
  {/if}
  
  <button disabled={!yes}>
    Subscribe
  </button>
</div>