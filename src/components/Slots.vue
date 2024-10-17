<template>
    <slot name="slotA" :task="task"></slot>
    <h1>
        Conponent Con
    </h1>
    <slot name="slotB"></slot>
    <h1>
        Conponent Con - 2
    </h1>
    <h3> vung ben duoi </h3>

    <slot name="slotC"></slot>
</template>

<script setup lang="ts">
let task = 'Hello'
</script>

<style scoped>

</style>