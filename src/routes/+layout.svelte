<script lang="ts">
import Navigation from '$lib/utility/navigation.svelte';
import Title from '$lib/utility/title.svelte';
import '../app.css';
let {
    children
} = $props();
</script>

<div class="flex flex-col lg:flex-row w-full h-full">
    <div class="flex flex-col w-full h-full lg:order-2">
        <Title />
        <div class="p-3 h-full">
            {@render children()}
        </div>
    </div>
    <Navigation />
</div>
