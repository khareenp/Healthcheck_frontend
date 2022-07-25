<script lang="ts">
	import { onMount } from 'svelte';
	import axios from 'axios';
	import EndpointsRow from './EndpointsRow.svelte';
	import Circle from './Circle.svelte';

	// const url =
	// 	process.env.NODE_ENV == 'production'
	// 		? 'https://healthcheck-api.modv.io/'
	// 		: 'http://localhost:7789/healthcheck/system';
	let healthcheckEndpoints: any[] = [];
	let promise: any;
	onMount(async function () {
		promise = axios
			// .get(url)
			.get('https://healthcheck-api.modv.io/')

			.then((response) => {
				healthcheckEndpoints = response.data;
				console.log(healthcheckEndpoints);

				return healthcheckEndpoints;
			})
			.catch((error) => {
				console.log({ error });
			});
	});
</script>

<div class=" space-y-4">
	{#await promise}
		<div />
	{:then healthcheckEndpoints}
		{#if healthcheckEndpoints?.length}
			{#each healthcheckEndpoints as endpoint, index}
				<EndpointsRow {...endpoint} />
			{/each}
		{/if}
	{:catch error}
		<p>oh dear.</p>
	{/await}
</div>
