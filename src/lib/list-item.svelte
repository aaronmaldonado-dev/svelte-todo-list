<script>
  import { items } from '../store';

  export let item;

  const removeItem = () => {
    items.update((prev) => prev.filter((i) => i.uuid !== item.uuid));
  };
</script>

<li class="item">
  <span class="item__content">{item.value}</span>
  <button class="item__btn" on:click={removeItem}>Remove</button>
</li>

<style>
  .item {
    background-color: #fff;
    margin-bottom: 1rem;
    border-radius: 3px;
    overflow: hidden;
    display: flex;
  }
  .item__content {
    text-transform: capitalize;
    color: #483e3e;
    padding: 0.5rem;
    flex: 1;
  }
  .item__btn {
    flex: 0 0 50px;
    cursor: pointer;
    border-radius: 0;
    color: #ffdedc;
    padding: 0 0.5rem;
    background-color: #f56468;
    border: 0px solid transparent;
  }
</style>
