<script setup>
import DownArrowIcon from './icons/IconDownArrow.vue'
import EllipseIcon from './icons/IconEllipse.vue'
</script>

<template>
    <section class="user">
        <EllipseIcon />
        <DownArrowIcon />
    </section>
</template>

<style scoped>
.user {
    display: flex;
    align-items: center;
    gap: 5px;
}
</style>
