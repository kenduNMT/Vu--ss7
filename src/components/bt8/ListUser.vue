<template>
    <div>
        <h2>Danh sách người dùng</h2>

        <button @click="toggleForm">Add user</button>

        <FormAddUser :isVisible="isFormVisible" @closeForm="toggleForm" />
    </div>
</template>

<script setup lang="ts">
import { ref } from 'vue';
import FormAddUser from './FormAddUser.vue';

const isFormVisible = ref(false);

function toggleForm() {
    isFormVisible.value = !isFormVisible.value;
}
</script>

<style scoped>
button {
    padding: 8px 12px;
    background-color: #007bff;
    color: white;
    border: none;
    border-radius: 4px;
    cursor: pointer;
}

button:hover {
    background-color: #0056b3;
}
</style>