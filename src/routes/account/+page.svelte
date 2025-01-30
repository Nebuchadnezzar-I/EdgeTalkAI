<script>
	import IdentifyCard from '$lib/aux/identify-card.svelte';
	import Subscription from '$lib/aux/subscription.svelte';
	import DocumentIcon from '$lib/icon/base/document-icon.svelte';
	import InfoSquareIcon from '$lib/icon/base/info-square-icon.svelte';
	import LockIcon from '$lib/icon/base/lock-icon.svelte';
	import LogoutIcon from '$lib/icon/base/logout-icon.svelte';
	import PaperIcon from '$lib/icon/base/paper-icon.svelte';
	import ShieldDoneIcon from '$lib/icon/base/shield-done-icon.svelte';
	import ShowIcon from '$lib/icon/base/show-icon.svelte';
	import ProfileIcon from '$lib/icon/profile-icon.svelte';
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

			<Subscription />
			
			<a href="/personal" class="btn btn-ghost w-full justify-start gap-3">
				<ProfileIcon />
				Personal Info
			</a>

			<a href="/security" class="btn btn-ghost w-full justify-start gap-3">
				<ShieldDoneIcon />
				Security
			</a>

			<a href="/language" class="btn btn-ghost w-full justify-start gap-3">
				<PaperIcon />
				Language
			</a>

			<a href="/theme" class="btn btn-ghost w-full justify-start gap-3">
				<ShowIcon />
				Theme
			</a>

			<!-- <Lang /> -->

			<div class="divider divider-start px-4 text-[14px]">About</div>

            <a href="/help" class="btn btn-ghost w-full justify-start gap-3">
				<DocumentIcon />
				Help Center
			</a>

            <a href="/privacy-policy" class="btn btn-ghost w-full justify-start gap-3">
				<LockIcon />
				Privacy Policy
			</a>

            <a href="/about" class="btn btn-ghost w-full justify-start gap-3">
				<InfoSquareIcon />
				About ChattyAI
			</a>

            <a href="/logout" class="btn btn-ghost w-full justify-start gap-3">
				<LogoutIcon />
				Logout
			</a>
		</div>
	</div>
</PagePadding>
