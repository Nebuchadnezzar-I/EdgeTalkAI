<script>
import PagePadding from "$lib/layout/page-padding.svelte";
import IdentityCard from "$lib/util/account/identity-card.svelte";
	import Link from "$lib/util/account/link.svelte";
</script>

<PagePadding>
    <div class="
        w-full h-full flex lg:items-center justify-center
        ">
        <div class="flex flex-col gap-3 h-min w-full max-w-[900px]">
            <IdentityCard />

            <div class="
                divider divider-start text-[14px] text-[#9E9E9E]
            ">General</div>

            <Link />
            <Link />
            <Link />
            <Link />

            <div class="
                divider divider-start text-[14px] text-[#9E9E9E]
            ">About</div>

            <Link />
            <Link />
            <Link />
            <Link />
        </div>
    </div>
</PagePadding>
