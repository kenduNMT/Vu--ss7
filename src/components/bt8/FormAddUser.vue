<template>
    <div v-if="isVisible" class="form-container">
        <h3>Thêm người dùng mới</h3>
        <form @submit.prevent="submitForm">
            <div>
                <label for="name">Name:</label>
                <input v-model="form.name" type="text" id="name" placeholder="Nhập tên" required>
            </div>
            <div>
                <label for="email">Email:</label>
                <input v-model="form.email" type="email" id="email" placeholder="Nhập email" required>
            </div>
            <div>
                <label for="address">Address:</label>
                <input v-model="form.address" type="text" id="address" placeholder="Nhập địa chỉ" required>
            </div>
            <div class="form-buttons">
                <button type="submit">Lưu</button>
                <button type="button" @click="closeForm">Close</button>
            </div>
        </form>
    </div>
</template>

<script setup lang="ts">
import { ref, defineProps, defineEmits } from 'vue';

const props = defineProps({
    isVisible: Boolean,
});

const emit = defineEmits(['closeForm']);

const form = ref({
    name: '',
    email: '',
    address: '',
});

function submitForm() {
    console.log('User Information:', form.value);
}

function closeForm() {
    emit('closeForm');
}
</script>

<style scoped>
.form-container {
    border: 1px solid #ccc;
    padding: 20px;
    margin-top: 20px;
    border-radius: 5px;
    width: 300px;
}

.form-buttons {
    display: flex;
    gap: 10px;
}

button {
    padding: 6px 10px;
    border: none;
    border-radius: 4px;
    cursor: pointer;
}

button[type="submit"] {
    background-color: #28a745;
    color: white;
}

button[type="button"] {
    background-color: #dc3545;
    color: white;
}
</style>