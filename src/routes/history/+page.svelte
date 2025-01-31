<script>
	import ArrowIcon from '$lib/icon/base/arrow-icon.svelte';
	import PagePadding from '$lib/layout/page-padding.svelte';
</script>

<PagePadding>
	<div class="flex h-full w-full lg:items-center lg:justify-center">
		<div
			class="
            flex h-full w-full flex-col
            gap-3 overflow-auto
            text-sm lg:max-h-[600px]
            lg:max-w-[800px] lg:gap-2
            "
		>
			<div class="flex h-full w-full flex-col overflow-auto scroll-content-2 gap-2 pr-2">
				{#each { length: 30 } as _, i}
					<div class="btn btn-ghost flex h-min justify-between p-3 px-6">
						<div class="flex flex-col gap-3 text-left">
							<h3 class="text-[18px] font-semibold">I weigh 70 kg, I want a diet plan to ...</h3>
							<p class="text-[10px] font-normal">29 Dec 2023 - 09:41 AM</p>
						</div>

						<ArrowIcon />
					</div>
				{/each}
			</div>
		</div>
	</div>
</PagePadding>
