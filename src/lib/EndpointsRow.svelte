<script lang="ts">
	import Date from '$lib/StartDate.svelte';
	import Time from '$lib/Time.svelte';
	import Circle from '$lib/Circle.svelte';

	export let node: string;
	export let version: string;
	export let startDate: string;
	export let endpoint: string;
	export let status: string;
</script>

<div>
	<div class="content flex justify-between  border-b-2 items-center px-2 py-2">
		<div class=" w-40 content__left flex flex-col ">
			<h2 class="uppercase font-semibold">{node}</h2>
			<p>{version}</p>
		</div>
		<div class="content__middle">
			<Date dateString={startDate} />
			<Time dateString={startDate} />
		</div>
		<div class=""><Circle {status} /></div>
	</div>
</div>
