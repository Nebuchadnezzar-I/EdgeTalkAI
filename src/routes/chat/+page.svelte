<script>
	import PagePadding from '$lib/layout/page-padding.svelte';
</script>

<PagePadding>
	<div
		class="
    flex h-full w-full flex-col items-center justify-between lg:pb-[40px]
"
	>
		<div></div>

		<div class="flex w-full max-w-[600px] flex-col items-center gap-6">
			<img class="h-[80px] w-[80px]" src="logo-small-bw.svg" alt="" />
			<h3
				class="
            text-2xl font-semibold
            text-[#BDBDBD]
            "
			>
				Capabilities
			</h3>

			<div class="flex w-full flex-col gap-3 text-center">
				<div
					class="
                cursor-pointer rounded-xl bg-[#F5F5F5]
                p-5 text-[#9E9E9E] duration-200 hover:bg-[#ebebeb]
            "
				>
					<p>
						Answer all your questions.<br />
						(Just ask me anything you like!)
					</p>
				</div>
				<div
					class="
                cursor-pointer rounded-xl bg-[#F5F5F5]
                p-5 text-[#9E9E9E] duration-200 hover:bg-[#ebebeb]
            "
				>
					<p>
						Generate all the text you want.<br />
						(essays, articles, reports, stories, & more)
					</p>
				</div>
				<div
					class="
                cursor-pointer rounded-xl bg-[#F5F5F5]
                p-5 text-[#9E9E9E] duration-200 hover:bg-[#ebebeb]
            "
				>
					<p>
						Conversational AI.<br />
						(I can talk to you like a natural human)
					</p>
				</div>
				<p class="text-[#9E9E9E]">
					These are just a few examples of what I can do.
				</p>
			</div>
		</div>

		<div class="flex w-full items-center gap-3">
			<input
				class="w-full rounded-2xl
            border-none bg-[#F5F5F5] px-4 py-4 text-[18px]
            outline-none focus:ring-0 lg:px-6 lg:py-5"
				type="text"
				placeholder="Ask me anything..."
			/>
			<a
				href="/chat"
				class="
            button-shaddow flex aspect-square
            h-[48px] items-center justify-center
            rounded-full bg-[--green] text-center duration-100 hover:bg-[--green-active] lg:h-[64px]
            "
			>
				<img src="icons/send.svg" alt="" />
			</a>
		</div>
	</div>
</PagePadding>
