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

			<Link img="icons/profile.svg" text="Personal Info" />
			<Link img="icons/shield-done.svg" text="Security" />
			<Link img="icons/document.svg" text="Language" />
			<Link img="icons/show.svg" text="Dark Mode" />

			<div class="divider divider-start px-4 text-[14px] text-[--text-secondary]">Default</div>

			<Link img="icons/paper.svg" text="Help Center" />
			<Link img="icons/lock.svg" text="Privacy Policy" />
			<Link img="icons/info-square.svg" text="About ChattyAI" />
			<Link img="icons/logout.svg" text="Logout" />
		</div>
	</div>
</PagePadding>
