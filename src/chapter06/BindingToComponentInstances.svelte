<script>
	import InputField from './BindingToComponentInstances/InputField.svelte';

  let field;
</script>

<div>
  <h1>06-14. Binding to component instances</h1>
  <p>DOM 요소에 바인딩할 수 있는 것처럼 구성 요소 인스턴스 자체에 바인딩할 수 있습니다. </p>
  <InputField bind:this={field} />

  <button on:click="{() => field.focus()}">
    Focus field
  </button>
</div>