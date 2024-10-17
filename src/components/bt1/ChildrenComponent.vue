<template>
    <div>
        <p>Tên công ty: {{ companyName }}</p>
    </div>
</template>

<script setup lang="ts">
interface Props {
    companyName: string
}
const props = defineProps<Props>()
</script>

<style scoped>
p {
    font-size: 18px;
    font-weight: bold;
    color: blue;
}
</style>