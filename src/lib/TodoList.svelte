<svelte:options immutable={true} />

<script>
    import { createEventDispatcher } from "svelte";

    export let todos = [];
    let inputText = ''

    const dispatch = createEventDispatcher()
    function handleAddTodo() {
        const isNotCancelled = dispatch(
            'addTodo', 
            { title: inputText }, 
            { cancelable: true }
        );
        if(isNotCancelled) { inputText = "" }
    }

    function handleRemoveTodo(id) {
        dispatch('removeTodo', { id });
    }

    function handleToggleTodo(id, value, event) {
        const newValue = !value;
        event.currentTarget.checked = newValue;
        dispatch('toggleTodo', { id, value: newValue });
    }
</script>

<div class="todo-list-wrapper">
    <ul>
        {#each todos as {id, title, completed} (id)}
            <li class="text-blue-500">
                <label>
                    <input 
                        on:input={(event) => handleToggleTodo(id, completed, event)}
                        type="checkbox" 
                        checked={completed}
                    />
                    {title}
                </label>
                <button 
                    on:click={() => handleRemoveTodo(id)} 
                    class="text-black bg-red-400 px-2 ml-2">
                    Remove
                </button>
            </li>
        {/each}
    </ul>   
    <form class="add-todo-form" on:submit|preventDefault={handleAddTodo}>
        <input class="text-black" bind:value={inputText}>
        <button 
            class="bg-blue-400 text-black px-4 ml-2" 
            type="submit" 
            disabled={!inputText}>
            Add
        </button>
    </form> 
</div> 



