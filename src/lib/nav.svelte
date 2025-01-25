<script lang="ts">
import NavLink from "./ui/nav-link.svelte";
import { onMount } from "svelte";

let pathName = $state<string>();

onMount(() => {
    pathName = window.location.pathname;
});
</script>

<div class="order-2 lg:order-1 px-8 py-6 flex lg:items-center">
    <div class="
        flex items-center text-center
        gap-5 justify-between w-full
        text-[10px] lg:text-[14px] text-[--text-secondary]
        lg:flex-col lg:gap-10
        ">

        <button onclick={() => pathName = "/home"}>
            <NavLink
                isActive={pathName === "/home"}
                link="/home"
                src="icons/Chat.svg"
                text="Chat"
            />
        </button>

        <button onclick={() => pathName = "/assistants"}>
            <NavLink
                isActive={pathName === "/assistants"}
                link="/assistants"
                src="icons/Category.svg"
                text="Assistants"
            />
        </button>

        <button onclick={() => pathName = "/history"}>
            <NavLink
                isActive={pathName === "/history"}
                link="/history"
                src="icons/Time-Circle.svg"
                text="History"
            />
        </button>

        <button onclick={() => pathName = "/account"}>
            <NavLink
                isActive={pathName === "/account"}
                link="/account"
                src="icons/Profile.svg"
                text="Account"
            />
        </button>
    </div>
</div>
