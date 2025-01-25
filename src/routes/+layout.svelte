<script lang="ts">
import '../app.css';
import Nav from "$lib/nav.svelte";
let { children } = $props();
</script>

<div class="w-full h-full flex flex-col lg:flex-row">
    <div class="
        w-full h-full order-1 lg:order-2
        lg:py-[40px]
    ">
        {@render children()}
    </div>

    <Nav />
</div>
