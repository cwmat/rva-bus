<script>
	import { AppBar } from '@skeletonlabs/skeleton';
</script>

<header>
	<AppBar
		gridColumns="grid-cols-3"
		slotDefault="place-self-center"
		slotTrail="place-content-end"
		class="bg-gradient-to-tr from-bg-primary-500 to-pink-500 transform"
	>
		<svelte:fragment slot="lead">🍔</svelte:fragment>
		<h3>
			🚌 <span
				class="bg-gradient-to-br from-pink-500 to-violet-500 bg-clip-text text-transparent box-decoration-clone font-extrabold"
				>RVA Bus Stuff</span
			>
		</h3>
		<svelte:fragment slot="trail">(actions)</svelte:fragment>
	</AppBar>
</header>
