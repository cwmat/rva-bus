<script lang="ts">
	import '../app.postcss';
	import './styles.css';
	import '@skeletonlabs/skeleton/themes/theme-skeleton.css';
	import '@skeletonlabs/skeleton/styles/all.css';
	import { AppShell } from '@skeletonlabs/skeleton';
	import Footer from '$lib/Footer.svelte';
	import Header from '$lib/Header.svelte';
	import Sidebar from '$lib/Sidebar.svelte';
</script>

<div class="app h-full w-full">
	<AppShell>
		<svelte:fragment slot="header"><Header /></svelte:fragment>
		<svelte:fragment slot="sidebarLeft"><Sidebar /></svelte:fragment>
		<!-- <svelte:fragment slot="sidebarRight">Sidebar Right</svelte:fragment> -->
		<!-- <svelte:fragment slot="pageHeader"><Header /></svelte:fragment> -->
		<!-- Router Slot -->
		<slot />
		<!-- ---- / ---- -->
		<!-- <svelte:fragment slot="pageFooter">Page Footer</svelte:fragment> -->
		<svelte:fragment slot="footer"><Footer /></svelte:fragment>
	</AppShell>
</div>