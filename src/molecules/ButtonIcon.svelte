<script>
    import Button from "../atoms/Button.svelte";
    import Icons from "../atoms/Icons.svelte";
</script>

<Button click={$$props.click} class={"flex items-center " + $$props.class ?? ""}>
    <Icons icon={$$props.icon} class="mr-2" />
    <slot></slot>
</Button>
