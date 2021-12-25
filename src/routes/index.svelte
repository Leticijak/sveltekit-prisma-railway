<script>
    import TodoItem from '../components/todo-item.svelte'

    const title = 'Todo | New'
</script>

<svelte:head>
    <title>{title}</title>
</svelte:head>

<h1>{title}</h1>


<form>
    <input type="text" name="text" aria-label='Add a todo' placeholder="+ type add a todo">
</form>

<TodoItem/>