<script setup>

defineProps({
    label: String,
    options: {
        type: Array,
        required: false,
    }
})
</script>

<template>
    <article class="content">
        <section class="knowledge--content">
            <article class="title--logo--content">
                <section class="title--logo">
                    <slot></slot>
                    <p class="title">{{ label }}</p>
                </section>
            </article>
            <article class="knowledge">
                <section class="knowledge--title" v-for="option in options">
                    <label>{{ option }}</label>
                </section>
            </article>
        </section>
    </article>
</template>

<style scoped>
.content {
    display: flex;
    align-items: flex-start;
    gap: 16px;
    flex: 1 0 0;
}

.knowledge--content {
    display: flex;
    padding: 16px;
    flex-direction: column;
    align-items: flex-start;
    gap: 16px;
    flex: 1 0 0;
    align-self: stretch;
    border-radius: 10px;
    border: 1px solid #E8EAF6;
}

.title--logo--content {
    display: flex;
    padding-bottom: 0px;
    align-items: center;
    gap: 8px;
    align-self: stretch;
}

.title--logo {
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

.knowledge {
    display: grid;
    grid-template-columns: repeat(4, 1fr);
    gap: 8px;
}

.knowledge--title {
    display: flex;
    width: 68px;
    padding: 0px 5px;
    justify-content: center;
    align-items: center;
    gap: 8px;
    border-radius: 10px;
    background: #E3F2FD;
}

label {
    color: #2196F3;
    text-align: center;
    font-family: Inter;
    font-size: 12px;
    font-style: normal;
    font-weight: 400;
    line-height: 150%;
    letter-spacing: 0.5px;
}
</style>
