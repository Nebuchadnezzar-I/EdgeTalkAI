<script lang="ts">
	let { SetTheme } = $props();
</script>

<button
	onclick={() => SetTheme('fantasy')}
	class="min-h-16 overflow-hidden rounded-lg border border-base-content/20 outline outline-2 outline-offset-2 outline-transparent hover:border-base-content/40"
	data-set-theme="fantasy"
	data-act-class="!outline-base-content"
>
	<div data-theme="fantasy" class="w-full cursor-pointer bg-base-100 font-sans text-base-content">
		<div class="grid grid-cols-5 grid-rows-3">
			<div class="col-start-1 row-span-2 row-start-1 bg-base-200"></div>
			<div class="col-start-1 row-start-3 bg-base-300"></div>
			<div
				class="col-span-4 col-start-2 row-span-3 row-start-1 flex flex-col gap-1 bg-base-100 p-2"
			>
				<div class="font-bold">fantasy</div>
				<div class="flex flex-wrap gap-1">
					<div class="flex aspect-square w-5 items-center justify-center rounded bg-primary lg:w-6">
						<div class="text-sm font-bold text-primary-content">A</div>
					</div>
					<div
						class="flex aspect-square w-5 items-center justify-center rounded bg-secondary lg:w-6"
					>
						<div class="text-sm font-bold text-secondary-content">A</div>
					</div>
					<div class="flex aspect-square w-5 items-center justify-center rounded bg-accent lg:w-6">
						<div class="text-sm font-bold text-accent-content">A</div>
					</div>
					<div class="flex aspect-square w-5 items-center justify-center rounded bg-neutral lg:w-6">
						<div class="text-sm font-bold text-neutral-content">A</div>
					</div>
				</div>
			</div>
		</div>
	</div>
</button>
