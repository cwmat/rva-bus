<script>
	import { AppBar } from '@skeletonlabs/skeleton';
</script>

<header>
	<AppBar gridColumns="grid-cols-3" slotDefault="place-self-center" slotTrail="place-content-end">
		<svelte:fragment slot="lead">🍔</svelte:fragment>
		🚌 RVA Bus Stuff
		<svelte:fragment slot="trail">(actions)</svelte:fragment>
	</AppBar>
</header>
