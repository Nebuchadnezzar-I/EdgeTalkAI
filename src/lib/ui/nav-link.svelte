<script lang="ts">
let {
    text,
    isActive
} = $props();

const icon =
    text === "Chat" ? "icons/chat.svg" :
    text === "AI Assistants" ? "icons/category.svg" :
    text === "History" ? "icons/time-circle.svg" :
    "icons/profile.svg";
</script>

<div class="
    flex flex-col items-center gap-1 rounded-xl
    text-[10px] hover:bg-[#eeeeee90]
    py-2 px-4 lg:py-3 lg:px-6 duration-200 cursor-pointer
    lg:w-[80px] {isActive ? "text-[--green]" : "text-[#9E9E9E]"}
    ">
    <img
        class="w-6 h-6"
        src={isActive ? icon.slice(0,-4) + "-active.svg" : icon}
        alt=""
        />
    <p>{text}</p>
</div>
