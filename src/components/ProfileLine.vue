<script setup>
defineProps({
    label: String
})
</script>

<template>
    <section class="content">
        <h2 class="title">{{ label }}</h2>
        <p class="line" />
    </section>
</template>

<style scoped>
.content {
    display: flex;
    padding: 10px 16px;
    align-items: center;
    gap: 16px;
    align-self: stretch;
    border-radius: 10px;
}

.title {
    color: #1A237E;
    text-align: center;
    font-family: Roboto;
    font-size: 20px;
    font-style: normal;
    font-weight: 700;
    line-height: 125%;
    letter-spacing: 0.5px;
}

.line {
    width: 100%;
    height: 1px;
    flex: 1 0 0;
    background: #E8EAF6;
}
</style>
