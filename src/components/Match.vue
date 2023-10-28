<script setup>
import Button from './Button.vue'
import BarIcon from './icons/IconBar.vue'
import UserPlusIcon from './icons/IconUserPlus.vue'
</script>

<template>
    <section class="match">
        <section class="match--content">
            <label class="match--title">Match con la cultura</label>
            <article class="match--bar">
                <label class="match--bar--name">80%</label>
                <article class="bar">
                    <BarIcon />
                </article>
            </article>
        </section>
        <section class="match--buttons">
            <Button label="Enviar Pitch">

            </Button>
            <Button label="Seguir" class="match--seguir">
                <UserPlusIcon />
            </Button>
        </section>
    </section>
</template>

<style scoped>
.match {
    display: flex;
    align-self: flex-start;
    position: relative;
    padding: 1rem 0rem;
    max-width: 806px;
    left: 115px;
    justify-content: space-between;
    align-items: center;
}

.match--content {
    display: flex;
    align-items: center;
    gap: 8px;
}

p {
    text-align: center;
    font-family: Inter;
    font-style: normal;
    line-height: 150%;
    letter-spacing: 0.5px;
}

.match--title {
    font-size: 13px;
    font-weight: 600;
    color: #9FA8DA;
}

.match--bar--name {
    font-size: 12px;
    font-weight: 400;
    color: #8BC34A;
}

.match--bar {
    display: flex;
    align-items: center;
    gap: 8px;
}

.bar {
    max-width: 276px;
    max-height: 14px;
}

.match--buttons {
    display: flex;
    height: 40px;
    justify-content: flex-end;
    align-items: center;
    gap: 10px;
}

.match--seguir{
    color: #DE1C7D;
    background-color: #FFF;
    border: 1.2px solid var(--principales-secondary-secondary-1, #DE1C7D);
}
</style>
