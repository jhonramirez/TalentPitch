<script setup lang="ts">

defineProps<{
    label: string,
}>()
</script>

<template>
    <button>
        <slot></slot>
        <p>{{ label }}</p>
    </button>
</template>

<style scoped>
button {
    display: flex;
    padding: 5px 12px;
    justify-content: center;
    align-items: center;
    border-radius: 5px;
    border-color: #DE1C7D;
    gap: 8px;
    background-color: #DE1C7D;
    color: #FFFBFC;
    cursor: pointer;
    flex-wrap: wrap-reverse;
}

p {
    font-size: 13px;
    font-style: normal;
    font-weight: 600;
    line-height: 150%;
    letter-spacing: 0.5px;
}
</style>
