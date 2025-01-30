<script lang="ts">
	import PagePadding from '$lib/layout/page-padding.svelte';
	import Acid from './options/acid.svelte';
	import Aqua from './options/aqua.svelte';
	import Autumn from './options/autumn.svelte';
	import Black from './options/black.svelte';
	import Bumblebee from './options/bumblebee.svelte';
	import Business from './options/business.svelte';
	import Cmyk from './options/cmyk.svelte';
	import Coffee from './options/coffee.svelte';
	import Corporate from './options/corporate.svelte';
	import Cupcake from './options/cupcake.svelte';
	import Cyberpunk from './options/cyberpunk.svelte';
	import Dark from './options/dark.svelte';
	import Dim from './options/dim.svelte';
	import Dracula from './options/dracula.svelte';
	import Emerald from './options/emerald.svelte';
	import Fantasy from './options/fantasy.svelte';
	import Forest from './options/forest.svelte';
	import Garden from './options/garden.svelte';
	import Halloween from './options/halloween.svelte';
	import Lemonade from './options/lemonade.svelte';
	import Light from './options/light.svelte';
	import Lofi from './options/lofi.svelte';
	import Luxury from './options/luxury.svelte';
	import Night from './options/night.svelte';
	import Nord from './options/nord.svelte';
	import Pastel from './options/pastel.svelte';
	import Retro from './options/retro.svelte';
	import Sunset from './options/sunset.svelte';
	import Synthwave from './options/synthwave.svelte';
	import Valentine from './options/valentine.svelte';
	import Winter from './options/winter.svelte';
	import Wireframe from './options/wireframe.svelte';

	function setTheme(name: string) {
		document.documentElement.setAttribute('data-theme', name);
		localStorage.setItem('theme', name);
	}
</script>

<PagePadding>
	<div class="flex h-full w-full lg:items-center lg:justify-center">
		<div
			class="
            scroll-content grid
            h-full min-h-96
            w-full grid-cols-2 gap-1
            overflow-auto lg:max-h-[600px]
            lg:max-w-[800px] lg:grid-cols-4 lg:gap-2
            lg:pr-2
        "
		>
			<Acid SetTheme={setTheme} />
			<Aqua SetTheme={setTheme} />
			<Autumn SetTheme={setTheme} />
			<Black SetTheme={setTheme} />
			<Bumblebee SetTheme={setTheme} />
			<Business SetTheme={setTheme} />
			<Cmyk SetTheme={setTheme} />
			<Coffee SetTheme={setTheme} />
			<Corporate SetTheme={setTheme} />
			<Cupcake SetTheme={setTheme} />
			<Cyberpunk SetTheme={setTheme} />
			<Dark SetTheme={setTheme} />
			<Dim SetTheme={setTheme} />
			<Dracula SetTheme={setTheme} />
			<Emerald SetTheme={setTheme} />
			<Fantasy SetTheme={setTheme} />
			<Forest SetTheme={setTheme} />
			<Garden SetTheme={setTheme} />
			<Halloween SetTheme={setTheme} />
			<Lemonade SetTheme={setTheme} />
			<Light SetTheme={setTheme} />
			<Lofi SetTheme={setTheme} />
			<Luxury SetTheme={setTheme} />
			<Night SetTheme={setTheme} />
			<Nord SetTheme={setTheme} />
			<Pastel SetTheme={setTheme} />
			<Retro SetTheme={setTheme} />
			<Sunset SetTheme={setTheme} />
			<Synthwave SetTheme={setTheme} />
			<Valentine SetTheme={setTheme} />
			<Winter SetTheme={setTheme} />
			<Wireframe SetTheme={setTheme} />
		</div>
	</div>
</PagePadding>
