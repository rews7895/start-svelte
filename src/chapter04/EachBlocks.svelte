<script>
  let cats = [
		{ id: 'J---aiyznGQ', name: 'Keyboard Cat' },
		{ id: 'z_AbfPXTKms', name: 'Maru' },
		{ id: 'OUtn3pvWmpg', name: 'Henri The Existential Cat' }
	];
</script>

<div>
  <h1>04-4. Each Blocks</h1>
  <p>데이터 목록을 반복해야 하는 경우 each블록을 사용</p>
  <p>destructuring을 사용할 수 있다.</p>
  <p># 유형1</p>
  {#each cats as cat, i}
    <li><a target="_blank" href="https://www.youtube.com/watch?v={cat.id}">{i + 1}. {cat.name}</a></li>
  {/each}
  <p># 유형2(destructuring 사용)</p>
  {#each cats as {id, name}, i}
    <li><a target="_blank" href="https://www.youtube.com/watch?v={id}">{i + 1}. {name}</a></li>
  {/each}
</div>