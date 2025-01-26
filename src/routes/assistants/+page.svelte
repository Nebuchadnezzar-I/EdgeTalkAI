<script>
import PagePadding from "$lib/layout/page-padding.svelte";
import Card from "$lib/util/assistants/card.svelte";
</script>

<PagePadding>
    <div class="
        w-full h-full flex lg:items-center justify-center
        ">
        <div class="grid grid-cols-2 gap-3 h-min w-full max-w-[900px]">
            <Card />
            <Card />
            <Card />
            <Card />
            <Card />
            <Card />
        </div>
    </div>
</PagePadding>
