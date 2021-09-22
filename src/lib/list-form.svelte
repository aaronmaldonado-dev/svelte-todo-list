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
  <input class="list-form__input" bind:value={val} />
  <button class="list-form__btn" type="submit" aria-label="Add Item">+</button>
</form>

<style>
  .list-form {
    height: 2.5rem;
    display: flex;
    width: 100%;
  }
  .list-form__input {
    border: 1px solid #bdbdbd;
    border-radius: 3px;
    margin-right: 1rem;
    font-size: 1rem;
    padding: 0 1rem;
    flex: 0 0 80%;
  }
  .list-form__btn {
    border: 1px solid #bdbdbd;
    background-color: #efefef;
    border-radius: 3px;
    font-size: 1.5rem;
    color: #828282;
    cursor: pointer;
    flex: 1;
  }
  .list-form__btn:hover {
    background-color: #e2e2e2;
  }
  .list-form__btn:active {
    background-color: #d5e0d5;
    border-color: #a1c1a1;
    color: #398c39;
  }
</style>
