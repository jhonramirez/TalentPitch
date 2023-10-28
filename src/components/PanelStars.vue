<script setup>
import StarActiveIcon from './icons/IconStarActive.vue'
import StarDisabledIcon from './icons/IconStarDisabled.vue'
</script>

<template>
    <section class="stars--content">
        <article class="stars--qualification">
            <StarActiveIcon />
            <StarActiveIcon />
            <StarActiveIcon />
            <StarActiveIcon />
            <StarDisabledIcon />
        </article>
        <h2 class="stars--reviews">(10 Reviews)</h2>
    </section>
</template>

<style scoped>
.stars--content {
    display: flex;
    justify-content: center;
    align-items: center;
    gap: 8px;
}

.stars--qualification {
    display: flex;
    max-width: 113.753px;
    align-items: flex-start;
    align-content: flex-start;
    gap: 0px 3.438px;
    flex-wrap: wrap;
}

.stars--reviews {
    font-size: 12px;
    font-weight: 400;
    letter-spacing: 0.5px;
    color: #666;
}
</style>
