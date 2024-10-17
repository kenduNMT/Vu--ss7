<template>
    <div>
        <MessageChildren @messageSent="handleMessage" />

        <p v-if="message">Bạn vừa nhận được một tin nhắn từ component con!</p>
    </div>
</template>

<script setup lang="ts">
import { ref } from 'vue';
import MessageChildren from './MessageChildren.vue';

const message = ref(false);

function handleMessage() {
    message.value = true;
}
</script>

<style scoped>
p {
    font-size: 16px;
    color: green;
    margin-top: 20px;
}
</style>