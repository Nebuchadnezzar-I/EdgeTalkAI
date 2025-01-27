<script lang="ts">
	import NavLink from './nav-link.svelte';
	import { onNavigate } from '$app/navigation';
	import { onMount } from 'svelte';

	let cp /* Current page */ = $state<string>();
	let ih /* Is nav hidden */ = $state<string>();

	onMount(() => {
		cp = window.location.pathname;
		ih = cp === '/chat' && window.screen.width < 700 ? 'hidden' : '';
	});

	onNavigate(() => {
		cp = window.location.pathname;
		ih = cp === '/chat' && window.screen.width < 700 ? 'hidden' : '';
	});
</script>

<div
	class="
    flex w-full items-center justify-center gap-3
    p-3 lg:w-fit lg:flex-col {ih}
    "
>
	<NavLink
		iconBaseName="chat"
		isActive={'/chat' === cp}
		link="/chat"
		className={ih}
		text="Chat"
	/>

	<NavLink
		iconBaseName="category"
		isActive={'/assistants' === cp}
		link="/assistants"
		className={ih}
		text="AI Assistants"
	/>

	<NavLink
		iconBaseName="time-circle"
		isActive={'/history' === cp}
		link="/history"
		className={ih}
		text="History"
	/>

	<NavLink
		iconBaseName="profile"
		isActive={'/account' === cp}
		link="/account"
		className={ih}
		text="Account"
	/>
</div>
