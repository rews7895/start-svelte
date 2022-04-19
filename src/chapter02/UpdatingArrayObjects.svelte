<script>
  let numbers = [1, 2, 3, 4];

  // function addNumber() {
  //   numbers.push(numbers.length + 1);
  //   numbers = numbers;
  // }
  function addNumber() {
    numbers = [...numbers, numbers.length + 1];
  }

  $: sum = numbers.reduce((t, n) => t + n, 0);
</script>

<div>
  <h1>02-4. Updating Arrays and Objects</h1>
  <p>반응형 변수는 할당에 의해 트리거되기 때문에 push, splice와 같은 것들로 업데이트가 발생하지 않는다.</p>
  <p>따라서 pop, shift, unshift, splice와 같은 것들을 사용한 후 업데이트를 해줘야한다.</p>
  <p>{numbers.join(' + ')} = {sum}</p>
  <button on:click={addNumber}>
    Add a number
  </button>
</div>
