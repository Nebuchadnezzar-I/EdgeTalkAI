<script lang="ts">
	type Props = {
		text: string;
		className: string | undefined;
		link: string;
		isActive: boolean;
		iconBaseName: string;
	};

	let { text, className, link, isActive, iconBaseName }: Props = $props();
</script>

<a
	href={link}
	class={`
	btn btn-ghost flex h-auto flex-col py-2 text-center text-[10px]
	font-medium hover:bg-transparent
	lg:w-[120px] lg:py-3 lg:text-[14px] lg:hover:bg-[--link-bg]
	${isActive ? 'text-[--green]' : 'text-[--text-secondary]'}
	${className}
`}
>
	<img src="icons/{iconBaseName}{isActive ? '-active' : ''}.svg" alt="" />
	{text}
</a>
