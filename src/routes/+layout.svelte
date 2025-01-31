<script lang="ts">
	import Header from '$lib/routing/header.svelte';
	import Nav from '$lib/routing/nav.svelte';
	import '../app.css';
	let { children } = $props();
</script>

<div class="h-full w-full flex flex-col">
	<Header />
	{@render children()}
	<Nav />
</div>
