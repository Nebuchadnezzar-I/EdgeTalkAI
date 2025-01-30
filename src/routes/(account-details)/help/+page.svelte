<script lang="ts">
	import SearchIcon from '$lib/icon/base/search-icon.svelte';
	import PagePadding from '$lib/layout/page-padding.svelte';

	type SlideState = 'faq' | 'cu';
	let currentSlide = $state<SlideState>('faq');

	let activeQuestion = $state(0);

	const questions = [
		{
			q: 'What is ChattyAI?',
			a: 'Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.'
		},
		{
			q: 'What is ChattyAI?',
			a: 'Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.'
		},
		{
			q: 'What is ChattyAI?',
			a: 'Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.'
		},
		{
			q: 'What is ChattyAI?',
			a: 'Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.'
		},
		{
			q: 'What is ChattyAI?',
			a: 'Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.'
		},
		{
			q: 'What is ChattyAI?',
			a: 'Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.'
		}
	];
</script>

<PagePadding>
	<div class="flex h-full w-full lg:items-center lg:justify-center">
		<div
			class="
            scroll-content-2 flex
            h-full w-full flex-col gap-3 overflow-auto
            pr-1 lg:max-h-[600px]
            lg:max-w-[800px] lg:gap-2 lg:pr-2
            "
		>
			<div class="flex w-full text-center">
				<button
					onclick={() => (currentSlide = 'faq')}
					class="
                    {currentSlide === 'faq' ? 'border-neutral' : 'border-transparent'}
                    w-full border-b-[3px] p-3 duration-200
                "
				>
					<p>FAQ</p>
				</button>

				<button
					onclick={() => (currentSlide = 'cu')}
					class="
                    {currentSlide === 'cu' ? 'border-neutral' : 'border-transparent'}
                    w-full border-b-[3px] p-3 duration-200
                "
				>
					<p>Contact us</p>
				</button>
			</div>

			{#if currentSlide === 'cu'}
				<div class="flex flex-col gap-3">
					<button class="btn btn-outline justify-start">Contact us</button>
                    <button class="btn btn-outline justify-start">WhatsApp</button>
                    <button class="btn btn-outline justify-start">Instagram</button>
                    <button class="btn btn-outline justify-start">Facebook</button>
                    <button class="btn btn-outline justify-start">Twitter</button>
                    <button class="btn btn-outline justify-start">Website</button>
				</div>
			{/if}

			{#if currentSlide === 'faq'}
				<div class="flex items-center gap-2 overflow-x-auto">
					<div class="badge h-7 px-4">General</div>
					<div class="badge h-7 px-4">Account</div>
					<div class="badge h-7 px-4">Service</div>
					<div class="badge h-7 px-4">Chatbot</div>
					<div class="badge h-7 px-4">Account</div>
					<div class="badge h-7 px-4">Service</div>
					<div class="badge h-7 px-4">Chatbot</div>
				</div>

				<div class="p-1">
					<label class="input input-bordered flex items-center gap-2">
						<SearchIcon svgClass="h-4 w-4 opacity-70" />
						<input
							class="box-border grow border-none outline-none focus:ring-0"
							type="text"
							placeholder="Search"
						/>
					</label>
				</div>

				<div class="join join-vertical w-full">
					{#each Object.entries(questions) as faq, i}
						<button
							onclick={() => (activeQuestion = i)}
							class="collapse join-item collapse-arrow border border-base-300 duration-300"
						>
							<input type="radio" name="my-accordion-4" checked={activeQuestion === i} />
							<div class="collapse-title text-left text-lg font-semibold">
								{faq[1].q}
							</div>
							<div class="collapse-content text-left text-sm">
								<p>
									{faq[1].a}
								</p>
							</div>
						</button>
					{/each}
				</div>
			{/if}
		</div>
	</div>
</PagePadding>
