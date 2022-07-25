<script lang="ts">
	export let status: string;
</script>

<div class="content__right">
	{#if status == 'Success'}
		<div class=" border-2 rounded-full w-6 h-6  bg-green-500" />
	{/if}
	{#if status == 'Warning'}
		<div class=" border-2 rounded-full w-6 h-6  bg-amber-500" />
	{/if}
	{#if status == 'Danger'}
		<div class=" border-2 rounded-full w-6 h-6  bg-red-500" />
	{/if}
</div>
