<template>
    <div class="app-container">
        <AddItemForm />
    </div>
</template>

<script>
    import AddItemForm from "./AddItemForm";
    export default {
        components: {
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
