<script lang="ts">
	import { page } from '$app/stores';
	import { onDestroy, onMount } from 'svelte';
  // import { Skeleton } from '@skeletonlabs/skeleton';

	// const type = $page.url.searchParams.get('type')!;
  const type = 'temp';
	let viewRef: HTMLDivElement;

	let cleanup: () => void;

  // const handleLightSwitch = (_event) => {
  //   // Handle the lightswitch event here
  //   console.log('Light switch toggled');
  // }

	onMount(async () => {
		const { init } = await import('$lib/services/mapping');
		cleanup = await init(viewRef, type);
    // const skeleton = new Skeleton({
    //   el: document.getElementById('skeleton'),
    //   events: {
    //     'lightswitch': handleLightSwitch
    //   }
    // });
	});

	onDestroy(() => {
		cleanup && cleanup();
	});
</script>

<div bind:this={viewRef} class="w-full h-full map" />
<!-- basemap="arcgis-dark-gray" -->

<style>
	.map {
		background-image: radial-gradient(
				at 0% 0%,
				rgba(var(--color-secondary-500) / 0.33) 0px,
				transparent 50%
			),
			radial-gradient(at 98% 1%, rgba(var(--color-error-500) / 0.33) 0px, transparent 50%);
	}
</style>
