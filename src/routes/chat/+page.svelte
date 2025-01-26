<script lang="ts">
type PageState = {
    isShowingWelcome: boolean;
}

let state = $state < PageState > ({
    isShowingWelcome: true,
});
</script>

<div class="
    w-full h-full flex flex-col justify-between items-center lg:pb-[40px]
    {!state.isShowingWelcome ? "" : "hidden"}    
">
    <div></div>

    <div class="max-w-[600px] w-full flex flex-col items-center gap-6">
        <img class="w-[80px] h-[80px]" src="logo-small-bw.svg" alt="">
        <h3 class="
            text-2xl text-[#BDBDBD]
            font-semibold
            ">
            Capabilities
        </h3>

        <div class="flex flex-col gap-3 w-full text-center">
            <div class="
                bg-[#F5F5F5] hover:bg-[#ebebeb] text-[#9E9E9E] 
                p-5 rounded-xl duration-200 cursor-pointer
            ">
                <p>
                    Answer all your questions.<br />
                    (Just ask me anything you like!)
                </p>
            </div>
            <div class="
                bg-[#F5F5F5] hover:bg-[#ebebeb] text-[#9E9E9E] 
                p-5 rounded-xl duration-200 cursor-pointer
            ">
                <p>
                    Generate all the text you want.<br />
                    (essays, articles, reports, stories, & more)
                </p>
            </div>
            <div class="
                bg-[#F5F5F5] hover:bg-[#ebebeb] text-[#9E9E9E] 
                p-5 rounded-xl duration-200 cursor-pointer
            ">
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

    <div class="flex items-center gap-3 w-full">
        <input
            class="px-4 py-4
            lg:px-6 lg:py-5 bg-[#F5F5F5] w-full text-[18px]
            border-none outline-none focus:ring-0 rounded-2xl"
            type="text" placeholder="Ask me anything..." />
        <a
            onclick={() => state.isShowingWelcome = false}
            href="/chat"
            class="
            bg-[--green] button-shaddow duration-100
            hover:bg-[--green-active] text-center rounded-full
            h-[48px] lg:h-[64px] aspect-square flex items-center justify-center
            ">
            <img src="icons/send.svg" alt="">
        </a>
    </div>
</div>

<div class="
    {!state.isShowingWelcome ? "hidden" : ""}
    flex items-center justify-center
    w-full h-full flex-col gap-10
    ">
    <img src="logo-big.svg" alt="" />

    <div class="flex flex-col gap-8">
        <h1 class="
            text-4xl font-semibold text-center
            ">
            Welcome to<br />
            <span class="text-[--green]">
                ChattyAI 👋
            </span>
        </h1>
        <p class="text-[18px] text-[#616161] text-center">
            Start chatting with ChattyAI now.<br />
            You can ask me anything.
        </p>
    </div>

    <a
        onclick={() => state.isShowingWelcome = false}
        href="/chat"
        class="
        font-semibold
        text-[18px] bg-[--green] text-white
        button-shaddow duration-100 py-4 px-5
        w-full max-w-[400px] rounded-full
        hover:bg-[--green-active] text-center
        ">
        Start Chat
    </a>
</div>
