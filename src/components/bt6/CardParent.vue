<template>
    <div>
        <Card>
            <template #header>
                Thông tin sản phẩm
            </template>

            <template #body>
                Đây là mô tả ngắn gọn về sản phẩm này. Sản phẩm có các tính năng nổi bật và giá cả hợp lý.
            </template>

            <template #footer>
                <button class="action-btn">Xem chi tiết</button>
            </template>
        </Card>
    </div>
</template>

<script setup lang="ts">
import Card from './Card.vue';
</script>

<style scoped>
.action-btn {
    padding: 8px 16px;
    background-color: #1890ff;
    color: white;
    border: none;
    border-radius: 4px;
    cursor: pointer;
}

.action-btn:hover {
    background-color: #40a9ff;
}
</style>