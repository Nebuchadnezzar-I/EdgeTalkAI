<script lang="ts">
let {
    src,
    text,
    link,
    isActive
} = $props();
</script>

<a href={link} class="
    flex flex-col gap-1 items-center cursor-pointer
    w-full h-full max-w-[80px] lg:max-w-[100px] max-h-[60px]
    duration-200 {isActive ? "text-[--green]" : ""}
">

    <img
        class="duration-200"
        alt="cha"
        src={
        isActive
            ? src.slice(0, -4) + "-Active.svg"
            : src
        }
    />

    <p>{text}</p>
</a>
