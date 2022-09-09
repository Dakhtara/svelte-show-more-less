<script lang="ts">
    import arrowDown from '../assets/icons/arrow-down.svg?raw';
    import arrowUp from '../assets/icons/arrow-up.svg?raw';
    export let icon: string;
    let icons = {
        'arrow-down': arrowDown,
        'arrow-up': arrowUp
    };

    //If icon in icons
    if (!icons[icon]) {
        console.error("No icons found for value " + icon);
    }
</script>

<div class={$$props.class} >
    {@html icons[icon]}
</div>
