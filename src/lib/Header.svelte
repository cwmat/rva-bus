<script lang="ts">
	import { AppBar, LightSwitch } from '@skeletonlabs/skeleton';
	// import { setContext } from 'svelte';
	// import { writable } from 'svelte/store';

	// // import type { LayoutData } from './$types';

	// export let data: any;
	// // Create a store and update it when necessary...
	// const darkMode = writable();
	// $: darkMode.set(data.darkMode);
	// // ...and add it to the context for child components to access
	// setContext('darkMode', darkMode);
</script>

<header class="header">
	<AppBar
		gridColumns="grid-cols-3"
		slotDefault="place-self-center"
		slotTrail="place-content-end"
		class="header"
	>
		<svelte:fragment slot="lead">🍔</svelte:fragment>
		<div class="text-lg md:text-3xl text-center">
			🚌 <span
				class="permanent-marker bg-gradient-to-br from-pink-500 to-violet-500 bg-clip-text text-transparent box-decoration-clone font-extrabold"
				>RVA Bus Stuff</span
			>🍑
		</div>
		<svelte:fragment slot="trail"><LightSwitch /></svelte:fragment>
	</AppBar>
</header>

<style>
	.header {
		background-image: radial-gradient(
				at 0% 0%,
				rgba(var(--color-secondary-500) / 0.33) 0px,
				transparent 50%
			),
			radial-gradient(at 98% 1%, rgba(var(--color-error-500) / 0.33) 0px, transparent 50%);
	}
</style>
