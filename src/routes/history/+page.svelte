<script>
	import ArrowIcon from '$lib/icon/base/arrow-icon.svelte';
	import PagePadding from '$lib/layout/page-padding.svelte';
</script>

<PagePadding>
	<div class="flex h-full w-full lg:items-center lg:justify-center">
		<div
			class="scroll-content flex h-full w-full flex-col gap-1 overflow-auto lg:max-h-[600px] lg:max-w-[800px] lg:gap-2 lg:pr-2"
		>
			{#each { length: 30 } as _, i}
				<div class="btn btn-ghost flex h-auto justify-between p-4">
					<div class="flex flex-col gap-3 text-left">
						<h3 class="text-[18px] font-semibold">I weigh 70 kg, I want a diet plan to ...</h3>
						<p class="text-[10px] font-normal">29 Dec 2023 - 09:41 AM</p>
					</div>

					<ArrowIcon />
				</div>
			{/each}
		</div>
	</div>
</PagePadding>
