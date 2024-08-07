<script lang="ts">
    import type { HTMLAttributes } from "svelte/elements";

    type CellProps = HTMLAttributes<HTMLDivElement> & {
        as?: "td" | "th";
    };

    let { as = "td", children }: CellProps = $props();
</script>

<svelte:element this={as}>
    {#if children}
        {@render children()}
    {/if}
</svelte:element>
