<template>
    <form class="form" @submit.prevent="onAddNewTask">
        <input class="input-field" type="text" placeholder="Enter task name" v-model="inputField" />
        <button>Submit</button>
    </form>
</template>

<script>
    import axios from 'axios';
    export default {
        data: () => ({
            inputField: '',
        }),
        methods: {
            async onAddNewTask() {
                if (this.inputField.trim()) {
                    await axios.post('api/item/store', {
                        item: {
                            name: this.inputField
                        }
                    });
                    this.inputField = '';
                }
            }
        }
    }
</script>

<style>
    .form {
        display: flex;
    }
    .input-field {
        width: 100%;
        padding: 10px 15px;
    }
    .input-field:focus {
        border: 2px solid green;
        outline: 0;
    }
</style>
