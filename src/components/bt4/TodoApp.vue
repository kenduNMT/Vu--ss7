<template>
    <div>
        <h2>-------- TodoApp Component --------</h2>
        <p>Id to delete: {{ todoIdToDelete }}</p>
        <TodoItem :id="1" @deleteTodo="handleDeleteTodo" />
    </div>
</template>

<script setup lang="ts">
import { ref } from 'vue';
import TodoItem from './TodoItem.vue';

const todoIdToDelete = ref<number | null>(null);

function handleDeleteTodo(id: number) {
    todoIdToDelete.value = id;
}
</script>

<style scoped>
h2,
h3 {
    font-size: 18px;
    margin: 0;
    padding-bottom: 10px;
}
</style>