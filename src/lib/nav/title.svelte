<script lang="ts">
	import { onNavigate } from '$app/navigation';
	import ArrowIcon from '$lib/icon/base/arrow-icon.svelte';
	import { onMount } from 'svelte';
	import { writable } from 'svelte/store';

	type TitleConf = {
		title: string;
		backLink: boolean;
		backLinkUrl: string;
	};

	const conf = $state<TitleConf>({
		title: '',
		backLink: false,
		backLinkUrl: ''
	});

	function configureTitle(path: string) {
		switch (path) {
			case '/':
				conf.title = 'ChattyAI';
				conf.backLink = false;
				break;

			case '/chat':
				conf.title = 'Chat';
				conf.backLink = false;
				break;

			case '/assistants':
				conf.title = 'AI Assistants';
				conf.backLink = false;
				break;

			case '/history':
				conf.title = 'History';
				conf.backLink = false;
				break;

			case '/account':
				conf.title = 'Account';
				conf.backLink = false;
				break;

			// Account details

			case '/about':
				conf.title = 'About';
				conf.backLink = true;
				conf.backLinkUrl = '/account';
				break;

			case '/help':
				conf.title = 'Help Center';
				conf.backLink = true;
				conf.backLinkUrl = '/account';
				break;

			case '/personal':
				conf.title = 'Personal Info';
				conf.backLink = true;
				conf.backLinkUrl = '/account';
				break;

			case '/privacy-policy':
				conf.title = 'Privacy Policy';
				conf.backLink = true;
				conf.backLinkUrl = '/account';
				break;

			case '/security':
				conf.title = 'Security';
				conf.backLink = true;
				conf.backLinkUrl = '/account';
				break;

			case '/theme':
				conf.title = 'Theme';
				conf.backLink = true;
				conf.backLinkUrl = '/account';
				break;

			case '/language':
				conf.title = 'Language';
				conf.backLink = true;
				conf.backLinkUrl = '/account';
				break;
		}
	}

	onMount(() => {
		configureTitle(window.location.pathname);
	});

	onNavigate(() => {
		configureTitle(window.location.pathname);
	});
</script>

<div class="flex items-center justify-between p-3">
	{#if conf.backLink}
		<a href={conf.backLinkUrl} class="btn btn-ghost w-[48px] p-0">
			<ArrowIcon svgClass="rotate-180" />
		</a>
	{:else}
		<a href="/" class="btn btn-ghost p-0 hover:bg-transparent">
			<img alt="" class="aspect-square w-[28px]" src="logo-small.svg" />
		</a>
	{/if}

	<h3 class="text-[24px] font-semibold">{conf.title}</h3>
	<div class="aspect-square w-[28px]"></div>
</div>
