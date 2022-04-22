<script>
	let questions = [
		{ id: 1, text: `Where did you go to school?` },
		{ id: 2, text: `What is your mother's name?` },
		{ id: 3, text: `What is another personal fact that an attacker could easily find with Google?` }
	];

	let selected;

	let answer = '';

	function handleSubmit() {
		alert(`answered question ${selected.id} (${selected.text}) with "${answer}"`);
	}
</script>

<div>
  <h1>06-6. Select Bindings</h1>
  <p>select의 bind는 select자체에 bind:value로 해서 넣는다.</p>

  <h2>Insecurity questions</h2>
  <form on:submit|preventDefault={handleSubmit}>
    <select bind:value={selected} on:change="{() => answer = ''}">
      {#each questions as question}
        <option value={question}>
          {question.text}
        </option>
      {/each}
    </select>

    <input bind:value={answer}>

    <button disabled={!answer} type=submit>
      Submit
    </button>
  </form>

  <p>selected question {selected ? selected.id : '[waiting...]'}</p>
</div>

<style>
	input {
		display: block;
		width: 500px;
		max-width: 100%;
	}
</style>