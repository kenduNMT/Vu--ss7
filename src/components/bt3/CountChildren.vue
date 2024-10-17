<template>
    <div>
        <button @click="incrementCount">Increment</button>
    </div>
</template>

<script setup lang="ts">
const emit = defineEmits(['increment'])

function incrementCount() {
    emit('increment')
}
</script>

<style scoped>
button {
    font-size: 16px;
    padding: 8px 16px;
    background-color: blue;
    color: white;
    border: none;
    cursor: pointer;
}

button:hover {
    background-color: darkblue;
}
</style>