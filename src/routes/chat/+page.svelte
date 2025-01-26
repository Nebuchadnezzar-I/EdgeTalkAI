<script>
import PagePadding from "$lib/layout/page-padding.svelte";
import Chat from "$lib/util/chat/chat.svelte";
</script>

<PagePadding>
    <div class="
        w-full h-full flex items-center lg:justify-center
        ">
        <div class="
            flex flex-col gap-3 w-full max-w-[900px]
            h-full overflow-y-auto pr-2 lg:max-h-[700px]
            ">
            <Chat />
            <div class="flex items-center gap-3 p-1">
                <input
                    type="text"
                    placeholder="Type here"
                    class="input input-bordered w-full"
                    />
                <button class="btn btn-active btn-primary">Send</button>
            </div>
        </div>
    </div>
</PagePadding>
