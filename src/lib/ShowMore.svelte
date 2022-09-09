<script lang="ts">
    import {onMount} from "svelte";

    let showMoreText = "Show more";
    let showLessText = "Show less";

    let isOpen = false;
    let blockShowMore;

    onMount(() => {
        handleBlockChange();
    })
    const onClick = (): void => {
        isOpen = !isOpen;
        handleBlockChange();
    };

    const handleBlockChange = (): void => {
        if (isOpen) {
            blockShowMore.style.maxHeight = blockShowMore.scrollHeight + `px`;
        } else {
            blockShowMore.style.maxHeight = "100px";
        }
    }

</script>


<div bind:this={blockShowMore} class="overflow-y-hidden transition-all duration-500 ease-in-out">
    <slot></slot>
</div>

<div class="flex items-center justify-between">
    <hr class="bg-black w-full">
    <button on:click="{onClick}" class="px-2 py-1  w-full rounded">
        {#if isOpen }{showLessText}{:else}{showMoreText}{/if}
    </button>
    <hr class="w-full bg-black">
</div>
