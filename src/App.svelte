<script>
    import TodoList from "./lib/TodoList.svelte";
    import { v4 as uuid } from "uuid";


    let todos = [
        {
            id: uuid(),
            title: 'Critical thinking',
            completed: true,
            value: 85
        },
        {
            id: uuid(),
            title: 'Problem-solving',
            completed: true,
            value: 80
        },
        {
            id: uuid(),
            title: 'Attention to detail',
            completed: false,
            value: 90
        },
        {
            id: uuid(),
            title: 'Communication',
            completed: true,
            value: 95
        },
        {
            id: uuid(),
            title: 'Collaboration',
            completed: true,
            value: 95
        },
    ]

    function handleAddTodo(event) {
        // event.preventDefault();
        let newTodo = {
            id: uuid(),
            title: event.detail.title,
            completed: false,
            value: 100
        }
        todos = [...todos, newTodo]
    }

    function handleRemoveTodo(event) {
        todos = todos.filter((todo) => todo.id !== event.detail.id)  
    }
   

    function handleToggleTodo(event) {
        todos = todos.map(todo => 
            todo.id === event.detail.id ? {...todo, completed: event.detail.value} : {...todo}
        );
    }


</script>

<TodoList 
    {todos} 
    on:addTodo={handleAddTodo} 
    on:removeTodo={handleRemoveTodo} 
    on:toggleTodo={handleToggleTodo}
/>

<style></style>
