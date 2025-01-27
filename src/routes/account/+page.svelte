<script>
	import IdentifyCard from '$lib/aux/identify-card.svelte';
	import Link from '$lib/aux/link.svelte';
	import PagePadding from '$lib/layout/page-padding.svelte';
</script>

<PagePadding>
	<div
		class="
		flex h-full
		w-full lg:items-center lg:justify-center
	"
	>
		<div class="flex w-full flex-col gap-1 lg:max-w-[800px] lg:gap-2">
			<IdentifyCard />

			<Link text="Personal Info" />
			<Link text="Security" />
			<Link text="Language" />
			<Link text="Dark Mode" />

			<div
				class="divider divider-start px-4 text-[14px] text-[--text-secondary]"
			>
				Default
			</div>

			<Link text="Help Center" />
			<Link text="Privacy Policy" />
			<Link text="About ChattyAI" />
			<Link text="Logout" />
		</div>
	</div>
</PagePadding>
