<template>
    <div>
        <h1>This is children</h1>
        <h3>Đây là count: {{ count }}</h3>
        <h3>Giá trị của test: {{ test }}</h3>
        <h3>Nội dung: {{ stringTittle }}</h3>

        <li v-for="user in userList" :key="user.id">{{ user.id }}</li>
        <li v-for="user in userList" :key="user.id">{{ user.name }}</li>
    </div>
</template>

<script setup lang="ts">
import { PropType } from 'vue';
interface User {
    id: number,
    name: string
}

defineProps({
    count: {
        type: Number,
        required: true,
    },
    test: {
        type: Number,
        default: 10
    },
    userList: {
        type: Array as PropType<User[]>,
        required: true
    },

    stringTittle: {
        type: String,
        default: "none"
    }
})
</script>

<style scoped></style>