<script lang="ts">
import {
    onNavigate
} from "$app/navigation";
import {
    onMount
} from "svelte";

let cp /* Current page */ = $state < string > ();
let ih /* Is nav hidden */ = $state < string > ();

onMount(() => {
    cp = window.location.pathname;
    ih = cp === "/chat" && window.screen.width < 700 ? "hidden" : "";
});

onNavigate(() => {
    cp = window.location.pathname;
    ih = cp === "/chat" && window.screen.width < 700 ? "hidden" : "";
});
</script>

<div class="
    flex w-full lg:w-fit items-center p-3
    gap-3 justify-center lg:flex-col {ih}
    ">
    <a href="/chat" class="
        btn btn-ghost h-auto flex-col py-2 font-medium lg:w-[100px] text-[10px] lg:text-[14px] hover:bg-[#f2f2f2]
        {cp === "/chat" ? "text-[--green]" : "text-[#9E9E9E]"}
        ">
        <img src="icons/chat{cp === "/chat" ? "-active" : ""}.svg" alt="" />
        Chat
    </a>

    <a href="/assistants" class="
        btn btn-ghost h-auto flex-col py-2 font-medium lg:w-[100px] text-[10px] lg:text-[14px] hover:bg-[#f2f2f2]
        {cp === "/assistants" ? "text-[--green]" : "text-[#9E9E9E]"}
        ">
        <img src="icons/category{cp === "/assistants" ? "-active" : ""}.svg" alt="" />
        AI Assistants
    </a>

    <a href="/history" class="
        btn btn-ghost h-auto flex-col py-2 font-medium lg:w-[100px] text-[10px] lg:text-[14px] hover:bg-[#f2f2f2]
        {cp === "/history" ? "text-[--green]" : "text-[#9E9E9E]"}
        ">
        <img src="icons/time-circle{cp === "/history" ? "-active" : ""}.svg" alt="" />
        History
    </a>

    <a href="/account" class="
        btn btn-ghost h-auto flex-col py-2 font-medium lg:w-[100px] text-[10px] lg:text-[14px] hover:bg-[#f2f2f2]
        {cp === "/account" ? "text-[--green]" : "text-[#9E9E9E]"}
        ">
        <img src="icons/profile{cp === "/account" ? "-active" : ""}.svg" alt="" />
        Account
    </a>
</div>
