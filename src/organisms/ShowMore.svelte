<script lang="ts">
    import {onMount} from "svelte";
    import ButtonIcon from "../molecules/ButtonIcon.svelte";

    export let showMoreText = "Show more";
    export let showLessText = "Show less";

    let isOpen = false;
    let blockShowMore;
    let arrowIcon: string = 'arrow-down';

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
            arrowIcon = "arrow-up";
        } else {
            blockShowMore.style.maxHeight = "100px";
            arrowIcon = "arrow-down";
        }
    }

</script>


<div bind:this={blockShowMore} class="overflow-y-hidden transition-all duration-500 ease-in-out">
    <slot></slot>
</div>

<div class="flex items-center justify-between">
    <hr class="w-full bg-black">
    <ButtonIcon click="{onClick}" class="w-full" icon="{arrowIcon}">
        {#if isOpen }{showLessText}{:else}{showMoreText}{/if}
    </ButtonIcon>
    <hr class="w-full bg-black">
</div>
