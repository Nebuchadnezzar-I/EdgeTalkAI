<script lang="ts">
	import { onNavigate } from '$app/navigation';
	import { onMount } from 'svelte';

	let view = $state(0);
	let tx = $state('translate-x-[0px]');

	function getViewPoint(path: string): number {
		switch (path) {
			case '/':
				return 0;

			case '/exercises':
				return 1;

			case '/new':
				return 2;

			case '/account':
				return 3;

			case '/temp':
				return 4;
		}

		return 0;
	}

	function setViewPoint(idx: number) {
		switch (idx) {
			case 0:
				tx = 'translate-x-[-400px]';
				break;

			case 1:
				tx = 'translate-x-[-320px]';
				break;

			case 2:
				tx = 'translate-x-[-240px]';
				break;

			case 3:
				tx = 'translate-x-[-160px]';
				break;

			case 4:
				tx = 'translate-x-[-80px]';
				break;
		}
	}

	const links = [
		{ img: 'icons/home.svg', url: '/' },
		{ img: 'icons/docs.svg', url: '/exercises' },
		{ img: 'icons/add.svg', url: '/new' },
		{ img: 'icons/person.svg', url: '/account' },
		{ img: 'icons/paper.svg', url: '/temp' }
	];

	onNavigate(() => {
		setViewPoint(getViewPoint(window.location.pathname));
	});

	onMount(() => {
		setViewPoint(getViewPoint(window.location.pathname));
	});
</script>

<div
	class="
    z-1 fixed bottom-0 left-0 z-20
    flex w-full items-center
    justify-center gap-4 pb-8
"
>
	{#each links as link, idx}
		<a
			href={link.url}
			onclick={() => setViewPoint(idx)}
			class="invert-based-on-z fja z-10 aspect-square w-[64px]"
		>
			<img src={link.img} alt="" />
		</a>
	{/each}

	<div class="fixed w-[384px] overflow-hidden rounded-full">
		<div class="flex {tx} w-[864px] transition-all duration-300 ease-in-out">
			<div
				class="
				mr-4 h-[64px] w-[384px] rounded-full bg-[--bg-2]
			"
			></div>

			<div
				class="invert-based-on-z mr-4 aspect-square h-[64px] rounded-full bg-white
			"
			></div>

			<div
				class="
				h-[64px] w-[384px] rounded-full bg-[--bg-2]
			"
			></div>
		</div>
	</div>
</div>
