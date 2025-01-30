<script lang="ts">
	import { onNavigate } from '$app/navigation';
	import CategoryIcon from '$lib/icon/category-icon.svelte';
	import ChatIcon from '$lib/icon/chat-icon.svelte';
	import ProfileIcon from '$lib/icon/profile-icon.svelte';
	import TimeCircleIcon from '$lib/icon/time-circle-icon.svelte';
	import { onMount } from 'svelte';

	let cp /* Current page */ = $state<string>('');
	let ih /* Is nav hidden */ = $state<string>('');

	onMount(() => {
		cp = window.location.pathname;
		ih = cp === '/chat' && window.screen.width < 700 ? 'hidden' : '';
	});

	onNavigate(() => {
		cp = window.location.pathname;
		ih = cp === '/chat' && window.screen.width < 700 ? 'hidden' : '';
	});

	function getClassName(path: string) {
		return `
		btn btn-ghost h-auto
		flex-col gap-2 py-2 lg:w-[80px]
		text-[10px] lg:text-[14px] px-5 lg:px-0
		${cp === path ? 'font-medium' : 'font-light'}
	`;
	}
</script>

<div class="flex w-full items-center justify-center gap-3 p-3 lg:w-fit lg:flex-col {ih}">
	<a href="/assistants" class={getClassName('/assistants')}>
		<CategoryIcon isActive={cp === '/assistants'} />
		<p>New</p>
	</a>

	<a href="/chat" class={getClassName('/chat')}>
		<ChatIcon isActive={cp === '/chat'} />
		<p>Ongoing</p>
	</a>

	<a href="/history" class={getClassName('/history')}>
		<TimeCircleIcon isActive={cp === '/history'} />
		<p>Closed</p>
	</a>

	<a href="/account" class={getClassName('/account')}>
		<ProfileIcon isActive={cp === '/account'} />
		<p>Accout</p>
	</a>
</div>
