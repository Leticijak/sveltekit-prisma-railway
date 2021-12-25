<script>
	import TodoItem from '../components/todo-item.svelte';

	const title = 'Todo | New';
</script>

<svelte:head>
	<title>{title}</title>
</svelte:head>

<div class="todos">
	<h1>{title}</h1>

	<form class="new">
		<input type="text" name="text" aria-label="Add a todo" placeholder="+ type add a todo" />
	</form>

	<TodoItem />
	<TodoItem />
	<TodoItem />
</div>

<style>
	.todos {
		width: 100%;
		max-width: 45rem;
		margin: 4rem auto 0 auto;
	}
	.new {
		margin: 0 0 0.5rem 0;
	}
	.new input {
		font-size: 28px;
		width: 100%;
		padding: 0.5rem 1rem 0.3rem 1rem;
		border-radius: 10px;
		text-align: center;
		background: rgb(165, 165, 165);
		cursor: pointer;
		border: none;
	}
	.todos :global(input) {
		border: 1px solid transparent;
	}
	.todos :global(input:focus-visible) {
		box-shadow: inset 1px 1px 6px rgba(0, 0, 0, 0.1);
		border: 1px solid #f7906e !important;
		outline: none;
	}
</style>
