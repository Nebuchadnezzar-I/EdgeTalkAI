<script lang="ts">
	let { text, img } = $props();
</script>

<!-- svelte-ignore a11y_invalid_attribute -->
<a
	href="#"
	onclick={() => (document.getElementById('my_modal_3') as HTMLDialogElement).showModal()}
	class="btn btn-ghost w-full justify-start gap-3 hover:bg-[--secondary-bg]"
>
	<img src={img} alt="" />
	{text}
</a>

<dialog id="my_modal_3" class="modal">
	<div class="modal-box">
		<form method="dialog">
			<button class="btn btn-circle btn-ghost btn-sm absolute right-2 top-2">✕</button>
		</form>
		<h3 class="text-lg font-bold">Hello!</h3>
		<p class="py-4">Press ESC key or click on ✕ button to close</p>
	</div>
</dialog>
