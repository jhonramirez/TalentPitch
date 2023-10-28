<script setup>
defineProps({
    label: String
})
</script>

<template>
    <section class="content">
        <slot></slot>
        <h2 class="title">{{ label }}</h2>
    </section>
</template>

<style scoped>
.content {
    display: flex;
    max-width: 250px;
    align-items: center;
    gap: 8px;
}

.title {
    color: #1A237E;
    text-align: center;
    font-family: Inter;
    font-size: 17px;
    font-style: normal;
    font-weight: 700;
    line-height: 125%;
    letter-spacing: 0.5px;
}
</style>
