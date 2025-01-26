<script>
import NavLink from "$lib/ui/nav-link.svelte";
import {
    onMount
} from "svelte";

let currentPage = $state();

onMount(() => {
    currentPage = window.location.pathname;
});
</script>

<div class="
    flex items-center gap-3 justify-center
    lg:flex-col lg:text-center p-3
    ">

    <a
        href="/chat"
        onclick={() => currentPage = "/chat"}
        >
        <NavLink
            isActive={currentPage === "/chat"}
            text="Chat" />
    </a>

    <a
        href="/assistants"
        onclick={() => currentPage = "/assistants"}
        >
        <NavLink
            isActive={currentPage === "/assistants"}
            text="AI Assistants" />
    </a>

    <a
        href="/history"
        onclick={() => currentPage = "/history"}
        >
        <NavLink
            isActive={currentPage === "/history"}
            text="History" />
    </a>

    <a
        href="/account"
        onclick={() => currentPage = "/account"}
        >
        <NavLink
            isActive={currentPage === "/account"}
            text="Account" />
    </a>

</div>
