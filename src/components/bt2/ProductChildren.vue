<template>
    <div>
        <h2>Thông tin sản phẩm</h2>
        <p>ID: {{ product.id }}</p>
        <p>Tên sản phẩm: {{ product.name }}</p>
        <p>Giá: {{ product.price }} VND</p>
        <p>Số lượng: {{ product.quantity }}</p>
    </div>
</template>

<script setup lang="ts">
interface Product {
    id: number
    name: string
    price: number
    quantity: number
}

const props = defineProps<{ product: Product }>()
</script>

<style scoped>
h2 {
    font-size: 20px;
    color: green;
}

p {
    font-size: 16px;
}
</style>