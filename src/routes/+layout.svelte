<script lang="ts">
import Nav from '$lib/ui/nav.svelte';
import Title from '$lib/ui/title.svelte';
import '../app.css';

let {
    children
} = $props();
</script>

<div class="
    w-full h-full flex
    flex-col lg:flex-row
    ">
    <div class="
        w-full h-full flex flex-col
        lg:order-2
        ">
        <Title />
        {@render children()}
    </div>
    <Nav />
</div>
