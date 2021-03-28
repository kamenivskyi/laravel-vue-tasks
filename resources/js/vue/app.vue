<template>
    <div class="app-container">
        <AddItemForm />
        <TaskList />
    </div>
</template>

<script>
    import AddItemForm from "./AddItemForm";
    import TaskList from "./TaskList";

    export default {
        components: {
            TaskList,
            AddItemForm
        }
    }
</script>

<style>
    .app-container {
        width: 400px;
        max-width: 90%;
        margin: 0 auto;
    }
</style>
