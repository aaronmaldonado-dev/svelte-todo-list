<script>
  import Form from '$lib/list-form.svelte';
  import Items from '$lib/list-items.svelte';
</script>

<div class="todo-list">
  <Form />
  <Items />
</div>

<style>
  .todo-list {
    background: #f4f7fc;
    border-radius: 3px;
    max-width: 520px;
    padding: 1.5rem;
    margin: 0 auto;
  }
</style>
