<template>
    <div>
        <h3>-------- TodoItem Component --------</h3>
        <button @click="deleteTodo">Delete</button>
    </div>
</template>

<script setup lang="ts">
import { defineProps, defineEmits } from 'vue';

const props = defineProps({
    id: Number,
});

const emit = defineEmits(['deleteTodo']);

function deleteTodo() {
    emit('deleteTodo', props.id);
}
</script>

<style scoped>
button {
    padding: 6px 12px;
    background-color: #ff4d4f;
    color: white;
    border: none;
    border-radius: 4px;
    cursor: pointer;
}

button:hover {
    background-color: #ff7875;
}
</style>