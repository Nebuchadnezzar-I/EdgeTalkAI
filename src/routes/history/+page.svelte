<script>
	import RecordItem from '$lib/aux/record-item.svelte';
	import PagePadding from '$lib/layout/page-padding.svelte';
</script>

<PagePadding>
	<div
		class="
		flex h-full
		w-full lg:items-center lg:justify-center
	"
	>
		<div
			class="scroll-content flex h-full w-full flex-col gap-1 overflow-auto lg:max-h-[600px] lg:max-w-[800px] lg:gap-2 lg:pr-2"
		>
			<RecordItem />
			<RecordItem />
			<RecordItem />
			<RecordItem />

			<RecordItem />
			<RecordItem />
			<RecordItem />
			<RecordItem />

			<RecordItem />
			<RecordItem />
			<RecordItem />
			<RecordItem />

			<RecordItem />
			<RecordItem />
			<RecordItem />
			<RecordItem />
		</div>
	</div>
</PagePadding>
