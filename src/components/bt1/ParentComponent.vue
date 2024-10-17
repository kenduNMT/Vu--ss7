<template>
    <div>
        <h1>Parent Component</h1>
        <ChildrenComponent :companyName="company" />
    </div>
</template>

<script setup lang="ts">
import ChildrenComponent from './ChildrenComponent.vue'

const company = 'Rikkei Academy'
</script>

<style scoped>
h1 {
    font-size: 24px;
    color: green;
}
</style>