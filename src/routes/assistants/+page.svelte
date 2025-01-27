<script>
	import AppLink from '$lib/aux/app-link.svelte';
	import PagePadding from '$lib/layout/page-padding.svelte';
</script>

<PagePadding>
	<div
		class="
		flex h-full
		w-full lg:items-center lg:justify-center
	"
	>
		<div class="grid h-min w-full max-w-[800px] grid-cols-2 gap-3">
			<AppLink />
			<AppLink />
			<AppLink />
			<AppLink />
		</div>
	</div>
</PagePadding>
