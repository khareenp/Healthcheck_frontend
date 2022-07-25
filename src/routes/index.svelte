<script context="module" lang="ts">
	export const prerender = true;
</script>

<script lang="ts">
	import Endpoints from '$lib/Endpoints.svelte';
	import EndpointsRow from '$lib/EndpointsRow.svelte';
</script>

<svelte:head>
	<title>Home</title>
	<meta name="description" content="MODV Health Checker" />
</svelte:head>

<div class="body px-2 py-3">
	<Endpoints />
	<!-- <EndpointsRow /> -->
</div>
