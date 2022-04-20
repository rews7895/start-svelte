<script>
	async function getRandomNumber() {
		const res = await fetch(`https://svelte.dev/tutorial/random-number`);
		const text = await res.text();

		if (res.ok) {
			return text;
		} else {
			throw new Error(text);
		}
	}

	let promise = getRandomNumber();

	function handleClick() {
		promise = getRandomNumber();
	}
</script>


<div>
  <h1>04-6. Awaite Blocks</h1>
  <p>비동기 데이터를 처리해야할 때 마크업에서 직접 Promise의 값을 쉽게 기다릴 수 있다.</p>
  <p>Promise가 해결될 때까지 아무것도 표시하지 않을 수 있다(catch블록의 생략)</p>
  
  <button on:click={handleClick}>
    generate random number
  </button>
  
  {#await promise}
    <p>...waiting</p>
  {:then value}
    <p>The number is {value}</p>
  {:catch error}
    <p style="color: red">{error.message}</p>
  {/await}

  {#await promise then value}
    <p>the value is {value}</p>
  {/await}
</div>