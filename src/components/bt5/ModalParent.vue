<template>
    <div>
        <h1>App Component</h1>
        <button @click="showModal">Open Modal</button>

        <Modal v-if="isModalVisible" title="Thông báo từ hệ thống" @close="isModalVisible = false">
            <p>Đây là nội dung của modal. Bạn có thể đóng modal bằng cách nhấn vào nút 'Close'.</p>
        </Modal>
    </div>
</template>

<script setup lang="ts">
import { ref } from 'vue'
import Modal from './Modal.vue'

const isModalVisible = ref(false)

// Hàm mở modal
function showModal() {
    isModalVisible.value = true
}
</script>

<style scoped>
h1 {
    margin-bottom: 20px;
}

button {
    padding: 10px 20px;
    background-color: #28a745;
    color: white;
    border: none;
    border-radius: 5px;
    cursor: pointer;
}

button:hover {
    background-color: #218838;
}
</style>