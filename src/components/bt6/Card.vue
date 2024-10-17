<template>
    <div class="card">
        <div class="card-header">
            <slot name="header"></slot>
        </div>

        <div class="card-body">
            <slot name="body"></slot>
        </div>

        <div class="card-footer">
            <slot name="footer"></slot>
        </div>
    </div>
</template>

<script setup lang="ts">
</script>

<style scoped>
.card {
    border: 1px solid #ddd;
    border-radius: 8px;
    padding: 16px;
    box-shadow: 0 4px 8px rgba(0, 0, 0, 0.1);
    max-width: 400px;
    margin: 20px auto;
}

.card-header {
    font-size: 18px;
    font-weight: bold;
    margin-bottom: 12px;
}

.card-body {
    font-size: 16px;
    margin-bottom: 12px;
}

.card-footer {
    display: flex;
    justify-content: flex-end;
}
</style>