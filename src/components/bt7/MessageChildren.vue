<template>
    <div>
        <button @click="sendMessage">Send message</button>
    </div>
</template>

<script setup lang="ts">
import { defineEmits } from 'vue';

const emit = defineEmits(['messageSent']);

function sendMessage() {
    emit('messageSent');
}
</script>

<style scoped>
button {
    background-color: #007bff;
    color: white;
    border: none;
    padding: 8px 12px;
    border-radius: 4px;
    cursor: pointer;
}

button:hover {
    background-color: #0056b3;
}
</style>