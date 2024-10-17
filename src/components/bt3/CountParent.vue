<template>
    <div>
        <h1>Count: {{ count }}</h1>
        <!-- Sử dụng component CountChildren và lắng nghe sự kiện "increment" -->
        <CountChildren @increment="updateCount" />
    </div>
</template>

<script setup lang="ts">
import CountChildren from './CountChildren.vue'
import { ref } from 'vue'

const count = ref(0)

function updateCount() {
    count.value += 1
}
</script>

<style scoped>
h1 {
    font-size: 24px;
    color: green;
}
</style>