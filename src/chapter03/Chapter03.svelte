<script>
  import DeclaringProps from './DeclaringProps.svelte';
  import DefaultValues from './DefaultValues.svelte';
  import SpreadProps from './SpreadProps.svelte';

  const pkg = {
    name: 'svelte',
    version: 3,
    speed: 'blazing',
    website: 'https://svelte.dev'
  }
</script>

<DeclaringProps answer={42}/>
<DefaultValues/>
<!-- <SpreadProps name={pkg.name} version={pkg.version} speed={pkg.speed} website={pkg.website}/> -->
<SpreadProps {...pkg}/>