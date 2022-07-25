<script lang="ts">
	import Header from '$lib/header/Header.svelte';
	import '../app.css';
</script>

<Header />

<main class=" tracking-wide bg-neutral-100 h-full">
	<slot />
</main>

<!-- <footer class=" flex items-center justify-center tracking-wide p-4">
	<p>visit <a class=" font-semibold text-sky-600" href="https://api.modv.io/swagger/#/">api.modv.io/swagger</a></p>
</footer> -->

<!-- <style>
	main {
		flex: 1;
		width: 100%;
		max-width: 1024px;
		margin: 0 auto;
		box-sizing: border-box;
	}

	@media (min-width: 480px) {
		footer {
			padding: 40px 0;
		}
	}
</style> -->
