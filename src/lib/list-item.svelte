<script>
  import { items } from '../store';

  export let item;

  const removeItem = () => {
    items.update((prev) => prev.filter((i) => i.uuid !== item.uuid));
  };
</script>

<li>
  <span class="item-content">{item.value}</span>
  <button on:click={removeItem}>Remove</button>
</li>