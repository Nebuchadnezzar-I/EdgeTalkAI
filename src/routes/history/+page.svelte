<script>
import PagePadding from "$lib/layout/page-padding.svelte";
import Item from "$lib/util/history/item.svelte";
</script>

<PagePadding>
    <div class="
        w-full h-full flex items-center lg:justify-center
        ">
        <div class="
            flex flex-col gap-3 w-full max-w-[900px] content-max-h
            h-full overflow-y-auto pr-2 lg:max-h-[700px]
            ">
            <Item />
            <Item />
            <Item />
            <Item />
            <Item />
            <Item />
            <Item />
            <Item />
            <Item />
            <Item />
            <Item />
            <Item />
        </div>
    </div>
</PagePadding>
