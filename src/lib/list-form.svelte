<script>
  import { v1 as uuid } from 'uuid';
  import { items } from '../store';

  let val;

  const addItem = () => {
    if (val) {
      items.update((prev) => [...prev, { uuid: uuid(), value: val }]);
      val = '';
    }
  };
</script>

<form class="list-form" on:submit|preventDefault={addItem}>
  <input bind:value={val}>
  <button type="submit">Add Item</button>
</form>