<script>
  import { items } from '../store';
  import Item from '$lib/list-item.svelte';

  const removeAll = () => {
    items.set([]);
  }
  
</script>

{#if $items.length > 0}
  <div class="items__wrapper">
    <ul class="items__list">
      {#each $items as item}
        <Item {item} />
      {/each}
    </ul>
    <button class="items__btn" on:click={removeAll}>Clear all</button>
  </div>
{/if}

<style>
  .items__wrapper {
    text-align: center;
  }
  .items__list {
    text-align: left;
    margin-top: 2rem;
    list-style: none;
  }
  .items__btn {
    border: 0px solid transparent;
    color: #989898;
    background: none;
    margin-top: 3rem;
    cursor: pointer;
  }
</style>
