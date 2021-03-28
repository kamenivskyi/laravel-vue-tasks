<template>
    <ul class="taks-list">
        <li v-for="item in items" :key="item.id">{{ item.name }}</li>
    </ul>
</template>

<script>
    import axios from 'axios';

    export default {
        data: () => ({
            items: [],
        }),
        async mounted() {
           const response = await axios.get('/api/items');

           this.items = response.data;
        }
    }
</script>

<style>
    .task-list {

    }
</style>
