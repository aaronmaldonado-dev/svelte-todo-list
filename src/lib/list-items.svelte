<script>
  import { items } from '../store';
  import Item from '$lib/list-item.svelte';
</script>

{#if $items.length > 0}
  {#each $items as item}
    <Item {item} />
  {/each}
{/if}
