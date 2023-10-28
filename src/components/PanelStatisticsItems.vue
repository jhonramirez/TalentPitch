<script setup>
defineProps({
    options: {
        type: Array,
        required: false,
    }
})
</script>

<template>
    <section class="content">
        <section v-for="option in options" class="statistics--content">
            <article class="statistics--items">

                <p class="item--name">
                    {{ option.title }}
                </p>
                <p class="item--number">
                    {{ option.number }}
                </p>
            </article>
        </section>
    </section>
</template>

<style scoped>
.content {
    display: flex;
    flex-direction: column;
    align-items: flex-start;
    align-self: stretch;
    background: #FFFDFF;
}

.statistics--content {
    display: flex;
    padding: 16px 0px;
    flex-direction: column;
    align-items: flex-start;
    gap: 8px;
    align-self: stretch;
    border-bottom: 1px solid #E8EAF6;
    background: #FFFDFF;
}

.statistics--items {
    display: flex;
    justify-content: space-between;
    align-items: center;
    align-self: stretch;
}

p {
    font-style: normal;
    color: 666;
}

.item--name {
    font-size: 9px;
    font-weight: 600;
    line-height: 150%;
    letter-spacing: 1.5px;
    text-transform: uppercase;
}

.item--number {
    font-size: 17px;
    font-weight: 700;
    line-height: 125%;
    letter-spacing: 0.5px;
}
</style>
