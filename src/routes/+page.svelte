<script>
	import PagePadding from '$lib/layout/page-padding.svelte';
</script>

<PagePadding>
	<div
		class="
		flex h-full w-full
		flex-col items-center justify-center gap-10
		"
	>
		<img src="logo-big.svg" alt="" />

		<div class="flex flex-col gap-8">
			<h1
				class="
				text-center text-4xl font-semibold
				"
			>
				Welcome to<br />
				<span class="text-[--green]"> ChattyAI 👋 </span>
			</h1>
			<p class="text-center text-[18px] text-[#616161]">
				Start chatting with ChattyAI now.<br />
				You can ask me anything.
			</p>
		</div>

		<a
			href="/chat"
			class="
			button-shaddow btn btn-ghost h-auto
			w-full max-w-[400px] rounded-full
			bg-[--green] px-5 py-4 text-center
			text-[18px] font-semibold text-white
			duration-100 hover:bg-[--green-active]
			"
		>
			Start Chat
		</a>
	</div>
</PagePadding>
