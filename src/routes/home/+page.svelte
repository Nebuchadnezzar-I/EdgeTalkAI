<script lang="ts">
import Button from "$lib/ui/button.svelte"
</script>

<div class="
    flex justify-center items-center
    w-full h-full p-5
">

    <div class="
        max-w-[600px] flex flex-col gap-12
        items-center w-full
    ">
        <img
            class="w-[180px] aspect-square"
            alt="logo"
            src="icons/Logo.svg"
        />

        <div class="flex flex-col gap-8">
            <h3 class="text-center text-[40px] font-bold">
                <span>Welcome to</span>
                <br />
                <span class="
                    text-[--green]
                    ">ChattyAI</span>
            </h3>

            <p class="text-[18px] text-center font-light">
                Start chatting with ChattyAI now.<br />
                You can ask me anything.
            </p>
        </div>

        <Button text="Start Chat" />
    </div>
</div>
