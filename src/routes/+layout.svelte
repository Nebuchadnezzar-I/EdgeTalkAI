<script lang="ts">
	let { children } = $props();
	import Navigation from '$lib/nav/navigation.svelte';
	import Title from '$lib/nav/title.svelte';

	import '../app.css';
</script>

<div
	class="
    flex h-full w-full flex-col pb-4 lg:flex-row
	lg:pb-0
    "
>
	<div class="flex h-full w-full flex-col lg:order-1">
		<Title />
		{@render children()}
	</div>
	<Navigation />
</div>
