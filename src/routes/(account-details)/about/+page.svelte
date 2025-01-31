<script>
	import ArrowIcon from '$lib/icon/base/arrow-icon.svelte';
	import PagePadding from '$lib/layout/page-padding.svelte';

	const options = [
		'Job Vacancy',
		'Developer',
		'Partner',
		'Accessibility',
		'Terms of Use',
		'Feedback',
		'Rate us',
		'Visit Our Website',
		'Follow us on Social Media'
	];
</script>

<PagePadding>
	<div class="flex h-full w-full lg:items-center lg:justify-center">
		<div
			class="
            scroll-content-2 overflow-auto
            flex flex-col gap-3
            h-full w-full text-sm
            lg:max-h-[600px] lg:max-w-[800px]
            pr-1 lg:gap-2 lg:pr-2
            "
		>
			<img class="aspect-square w-[140px] mx-auto" src="logo-small.svg" alt="" />

			<h3 class="text-2xl font-semibold mx-auto">ChattyAI v0.0.0</h3>

			<div class="flex flex-col gap-1">
				{#each Object.entries(options) as option}
					<button class="btn btn-ghost flex items-center justify-between">
						{option[1]}
						<ArrowIcon />
					</button>
				{/each}
			</div>
		</div>
	</div>
</PagePadding>
