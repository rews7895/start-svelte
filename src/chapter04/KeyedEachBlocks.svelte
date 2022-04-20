<script>
  import Thing from "./KeyedEachBlocks/Thing.svelte";

  let things = [
		{ id: 1, name: 'apple' },
		{ id: 2, name: 'banana' },
		{ id: 3, name: 'carrot' },
		{ id: 4, name: 'doughnut' },
		{ id: 5, name: 'egg' },
	];

	function handleClick() {
		things = things.slice(1);
	}
</script>

<div>
  <h1>04-5. Keyed Each Blocks</h1>
  <p>어떠한 액션(제거와 같은) 것들을 하면서 다른 구성 요소들에는 영향을 받지 않도록 하기 위해서는 each 블록에 고유 식별자(또는 키)를 지정해야 한다.</p>
  <p>고유 식별자는 문자열이나 숫자를 사용.</p>
</div>

<button on:click={handleClick}>
	Remove first thing
</button>

{#each things as thing (thing.id)}
	<Thing name={thing.name}/>
{/each}