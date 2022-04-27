<script>
  import { onMount } from 'svelte';

	let photos = [];
  
  onMount(async () => {
		const res = await fetch(`/tutorial/api/album`);
		photos = await res.json();
	});

</script>

<div>
  <h1>07-1. onMount</h1>
  <p>onMount는 컴포넌트가 DOM에 처음 렌더링된 후 실행되는 것.</p>
  <p>서버측 렌더링(SSR) 때문에 스크립트의 최상위 레벨보다는 마운트에 페치를 넣는 것이 좋다.</p>
  <p>OnDestroy를 제외하고 SSR 중에는 라이프사이클 기능이 실행되지 않습니다.</p>
  <h1>Photo album</h1>
  <div class="photos">
    {#each photos as photo}
      <figure>
        <img src={photo.thumbnailUrl} alt={photo.title}>
        <figcaption>{photo.title}</figcaption>
      </figure>
    {:else}
      <p>loading...</p>
    {/each}
  </div>
</div>

<style>
	.photos {
		width: 100%;
		display: grid;
		grid-template-columns: repeat(5, 1fr);
		grid-gap: 8px;
	}

	figure, img {
		width: 100%;
		margin: 0;
	}
</style>