<script lang="ts">
	import { darkMode } from '$lib/stores/darkMode';
	import { AppBar, LightSwitch } from '@skeletonlabs/skeleton';

	const handleLightSwitch = (_event: any) => {
		console.log('lightswitch toggle')
		darkMode.update(e => !e);
	};
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
		<svelte:fragment slot="trail"><LightSwitch on:click={handleLightSwitch} /></svelte:fragment>
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
