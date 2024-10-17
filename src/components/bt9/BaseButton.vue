<template>
    <button :type="type" class="base-button" @click="handleClick">
        <slot>{{ children }}</slot>
    </button>
</template>

<script>
export default {
    name: 'BaseButton',

    props: {
        children: {
            type: String,
            default: ''
        },

        type: {
            type: String,
            default: 'button',
            validator: function (value) {
                return ['submit', 'button', 'reset'].includes(value)
            }
        },

        onClick: {
            type: Function,
            default: null
        }
    },

    methods: {
        handleClick(event) {
            this.$emit('click', event)
            if (this.onClick) {
                this.onClick(event)
            }
        }
    }
}
</script>

<style scoped>
.base-button {
    background-color: #3498db;
    color: white;
    border: none;
    border-radius: 6px;
    padding: 10px 40px;
    font-size: 16px;
    cursor: pointer;
    min-width: 120px;
    transition: background-color 0.3s;
}

.base-button:hover {
    background-color: #2980b9;
}

.base-button:active {
    background-color: #2472a4;
}
</style>