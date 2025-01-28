<script lang="ts">
	import { onNavigate } from '$app/navigation';
	import { onMount } from 'svelte';

	let cp /* Current page */ = $state<string>();

	function getHeadText(path: string) {
		switch (path) {
			case '/':
				cp = 'ChattyAI';
				break;
			case '/chat':
				cp = 'ChattyAI';
				break;
			case '/assistants':
				cp = 'AI Assistants';
				break;
			case '/history':
				cp = 'History';
				break;
			case '/account':
				cp = 'Account';
		}
	}

	onMount(() => {
		getHeadText(window.location.pathname);
	});

	onNavigate(() => {
		getHeadText(window.location.pathname);
	});
</script>

<div
	class="
    flex items-center justify-between p-3
"
>
	<a href="/" class="btn btn-ghost p-0 hover:bg-transparent"
		><img class="aspect-square w-[28px]" src="logo-small.svg" alt="" /></a
	>
	<h3 class="text-[24px] font-semibold">{cp}</h3>
	<div class="aspect-square w-[28px]"></div>
</div>
