<script>
	import ArrowIcon from '$lib/icon/base/arrow-icon.svelte';
	import PagePadding from '$lib/layout/page-padding.svelte';
</script>

<PagePadding>
	<div class="flex h-full w-full lg:items-center lg:justify-center">
		<div
			class="
            scroll-content-2 flex
            h-full w-full flex-col
            gap-3 overflow-auto pr-1
            text-sm lg:max-h-[600px]
            lg:max-w-[800px] lg:gap-2 lg:pr-2
            "
		>
			<div class="form-control w-full">
				<label class="label cursor-pointer">
					<span class="label-text">Remember me</span>
					<input type="checkbox" class="toggle" />
				</label>
			</div>

			<div class="form-control w-full">
				<label class="label cursor-pointer">
					<span class="label-text">Face ID</span>
					<input type="checkbox" class="toggle" />
				</label>
			</div>

			<div class="form-control w-full">
				<label class="label cursor-pointer">
					<span class="label-text">SMS Authenticator</span>
					<input type="checkbox" class="toggle" />
				</label>
			</div>

			<div class="form-control w-full">
				<label class="label cursor-pointer">
					<span class="label-text">Google Authenticator</span>
					<input type="checkbox" class="toggle" />
				</label>
			</div>

			<div class="form-control w-full">
				<label class="label cursor-pointer">
					<span class="label-text">Device Management</span>
					<input type="checkbox" class="toggle" />
				</label>
			</div>

			<button class="btn btn-outline w-full lg:max-w-[300px]"> Change password </button>
		</div>
	</div>
</PagePadding>
