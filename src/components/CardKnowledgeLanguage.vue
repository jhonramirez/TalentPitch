<script setup>

defineProps({
    label: String,
    options: Array
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
                <section class="knowledge--title--subtitle" v-for="option in options">
                    <h2>{{ option.title }}</h2>
                    <h3>{{ option.subtitle }}</h3>
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
    display: flex;
    align-items: flex-end;
    gap: 8px;
    align-self: stretch;
}

.knowledge--title--subtitle {
    display: flex;
    flex-direction: column;
    align-items: flex-start;
    gap: 3px;
    flex: 1 0 0;
}

h2 {
    color: #212121;
    font-family: Inter;
    font-size: 13px;
    font-style: normal;
    font-weight: 600;
    line-height: 150%;
    letter-spacing: 0.5px;
}

h3 {
    display: flex;
    width: 103px;
    height: 14px;
    flex-direction: column;
    justify-content: center;
    color: #A1A1A1;
    font-family: Inter;
    font-size: 12px;
    font-style: normal;
    font-weight: 400;
    line-height: 150%;
    letter-spacing: 0.5px;
}
</style>
