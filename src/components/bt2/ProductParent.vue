<template>
    <div>
        <h1>Product Parent Component</h1>
        <!-- Truyền dữ liệu product xuống component con qua props -->
        <ProductChildren :product="product" />
    </div>
</template>

<script setup lang="ts">
import ProductChildren from './ProductChildren.vue'

const product = {
    id: 1,
    name: 'Laptop Dell XPS',
    price: 30000000,
    quantity: 2
}
</script>

<style scoped>
h1 {
    font-size: 24px;
    color: blue;
}
</style>