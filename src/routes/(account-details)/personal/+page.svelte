<script>
	import PagePadding from '$lib/layout/page-padding.svelte';
</script>

<PagePadding>
	<div class="flex h-full w-full lg:items-center lg:justify-center">
		<div
			class="
            scroll-content-2 flex
            h-full w-full flex-col
            items-center gap-1 overflow-auto
            pr-1 text-sm lg:max-h-[600px]
            lg:max-w-[800px] lg:gap-2 lg:pr-2
            "
		>
			<div class="avatar">
				<div class="w-24 rounded-full">
					<img
						alt=""
						src="https://img.daisyui.com/images/stock/photo-1534528741775-53994a69daeb.webp"
					/>
				</div>
			</div>

			<label class="form-control w-full px-1">
				<div class="label">
					<span class="label-text">Full Name</span>
				</div>
				<input value="Andrew Ainsley" type="text" class="input input-bordered w-full" />
			</label>

			<label class="form-control w-full px-1">
				<div class="label">
					<span class="label-text">Email</span>
				</div>
				<input
					value="andrew.ainsley@yourdomain.com"
					type="text"
					class="input input-bordered w-full"
				/>
			</label>

			<label class="form-control w-full px-1">
				<div class="label">
					<span class="label-text">Phone Number</span>
				</div>
				<input value="+1 111 467 378 399" type="text" class="input input-bordered w-full" />
			</label>

			<label class="form-control w-full px-1">
				<div class="label">
					<span class="label-text">Phone Number</span>
				</div>
				<select class="select input-bordered w-full">
					<option disabled selected>Pick your favorite Simpson</option>
					<option>Homer</option>
					<option>Marge</option>
					<option>Bart</option>
					<option>Lisa</option>
					<option>Maggie</option>
				</select>
			</label>

			<label class="form-control w-full px-1">
				<div class="label">
					<span class="label-text">Date of Birth</span>
				</div>
				<input value="12/27/1995" type="text" class="input input-bordered w-full" />
			</label>

			<label class="form-control w-full px-1">
				<div class="label">
					<span class="label-text">Street Address</span>
				</div>
				<input
					value="3517 W. Gray Street, New York"
					type="text"
					class="input input-bordered w-full"
				/>
			</label>

			<label class="form-control w-full px-1">
				<div class="label">
					<span class="label-text">Country</span>
				</div>
				<select class="select input-bordered w-full">
					<option disabled selected>US</option>
					<option>Homer</option>
					<option>Marge</option>
					<option>Bart</option>
					<option>Lisa</option>
					<option>Maggie</option>
				</select>
			</label>
		</div>
	</div>
</PagePadding>
