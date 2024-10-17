<template>
    <div v-if="isVisible" class="modal-overlay">
        <div class="modal-container">
            <div class="modal-header">
                <h2>{{ title }}</h2>
            </div>
            <div class="modal-body">
                <slot></slot>
            </div>
            <div class="modal-footer">
                <button @click="closeModal">Close</button>
            </div>
        </div>
    </div>
</template>

<script setup lang="ts">
import { ref } from 'vue';

const props = defineProps<{ title: string }>()
const emit = defineEmits(['close'])

const isVisible = ref(true)

function closeModal() {
    isVisible.value = false
    emit('close')
}
</script>

<style scoped>
.modal-overlay {
    position: fixed;
    top: 0;
    left: 0;
    width: 100%;
    height: 100%;
    background: rgba(0, 0, 0, 0.5);
    display: flex;
    justify-content: center;
    align-items: center;
}

.modal-container {
    background-color: white;
    padding: 20px;
    border-radius: 10px;
    width: 400px;
    text-align: center;
}

.modal-header {
    margin-bottom: 20px;
}

.modal-body {
    margin-bottom: 20px;
}

.modal-footer {
    margin-top: 20px;
}

button {
    padding: 10px 20px;
    background-color: #007bff;
    color: white;
    border: none;
    border-radius: 5px;
    cursor: pointer;
}

button:hover {
    background-color: #0056b3;
}
</style>