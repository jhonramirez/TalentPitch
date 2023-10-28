<script setup>
import Button from './Button.vue'
import StartCardIcon from './icons/IconStartCard.vue'
import ShareAltCardIcon from './icons/IconShareAltCard.vue'
import LineIcon from './icons/IconLine.vue'
defineProps({
    infoCard: Object,
})
</script>

<template>
    <article class="card">
        <img alt="TalentPitch Card1" class="logo" v-bind:src="infoCard.image" width="236" height="73" />
        <article class="card--header">
            <section class="card--header--qualification">
                <h2 class="header--title">Experticia</h2>
                <StartCardIcon />
            </section>
            <ShareAltCardIcon />
        </article>
        <section class="card--content">
            <article class="card--content--info">
                <section class="info">
                    <section class="info--title">
                        <h2 class="title">{{ infoCard.name }}</h2>
                        <section class="info--subtitle">
                            <h3 class="subtitle">Creada por organización: {{ infoCard.company_name }}</h3>
                        </section>
                    </section>
                    <p class="info--description">{{ infoCard.description }}</p>
                </section>
                <section class="card--statistics">
                    <article class="card--statistics--items">
                        <section class="statistics--circle">
                            <p class="statistics--number">{{ infoCard.views_count }}</p>
                        </section>
                        <h3 class="statistics--title">Vistas</h3>
                    </article>
                    <article class="card--statistics--items">
                        <section class="statistics--circle">
                            <p class="statistics--number">{{ infoCard.comments_count }}</p>
                        </section>
                        <h3 class="statistics--title">Comentarios</h3>
                    </article>
                    <article class="card--statistics--items">
                        <section class="statistics--circle">
                            <p class="statistics--number">{{ infoCard.pitches_count }}</p>
                        </section>
                        <h3 class="statistics--title">Pitches</h3>
                    </article>
                </section>
            </article>
            <LineIcon />
            <Button label="Aplicar a vacante" />
        </section>
    </article>
</template>

<style scoped>
.card {
    display: flex;
    margin: 1rem;
    flex-direction: column;
    justify-content: center;
    align-items: flex-start;
    flex: 1 0 0;
    border-radius: 10px;
    border: 1px solid #E8EAF6;
    background: #FFF;
    position: relative;
    left: 115px;
}

.card--header {
    display: flex;
    padding: 8px 12px;
    width: 100%;
    justify-content: space-between;
    align-items: center;
    background: #FAFAFA;
}

.logo {
    border-radius: 10px 10px 0 0;
}

.card--header--qualification {
    display: flex;
    align-items: center;
    gap: 8px;
}

.header--title {
    color: #666;
    font-family: Roboto;
    font-size: 12px;
    font-style: normal;
    font-weight: 400;
    line-height: 150%;
    letter-spacing: 0.5px;
}

.card--content {
    display: flex;
    width: 236px;
    padding: 11px 12px 12px 12px;
    flex-direction: column;
    align-items: flex-start;
    gap: 16px;
}

.card--content--info {
    display: flex;
    flex-direction: column;
    align-items: flex-start;
    gap: 16px;
    align-self: stretch;
}

.info {
    display: flex;
    flex-direction: column;
    align-items: flex-start;
    gap: 8px;
    align-self: stretch;
}

.info--title {
    display: flex;
    flex-direction: column;
    align-items: flex-start;
    gap: 5px;
}

.title {
    color: #1A237E;
    max-width: 272px;
    font-family: Roboto;
    font-size: 16px;
    font-style: normal;
    font-weight: 400;
    line-height: 162%;
    letter-spacing: 0.5px;
    height:50px ;
}

.info--subtitle {
    display: flex;
    padding: 0px 5px;
    justify-content: center;
    align-items: center;
    gap: 8px;
    border-radius: 10px;
    background: #E3F2FD;
}

.subtitle {
    color: var(--colores-semnticos-info-info-1, #2196F3);
    text-align: center;
    font-family: Roboto;
    font-size: 12px;
    font-style: normal;
    font-weight: 400;
    line-height: 150%;
    letter-spacing: 0.5px;
}

.info--description {
    color: #666;
    max-width: 100%;
    font-family: Roboto;
    font-size: 12px;
    font-style: normal;
    font-weight: 400;
    line-height: 150%;
    letter-spacing: 0.5px;
    text-align: start;
    height: 72px;
    overflow-y: hidden;
}

.card--statistics {
    display: flex;
    justify-content: space-between;
    align-items: center;
    align-self: stretch;
}

.card--statistics--items {
    display: flex;
    flex-direction: column;
    align-items: center;
    gap: 5px;
}

.statistics--title {
    color: #666;
    font-family: Roboto;
    font-size: 11px;
    font-style: normal;
    font-weight: 500;
    line-height: 120%;
    letter-spacing: 0.5px;
}

.statistics--circle {
    display: flex;
    padding: 0px 5px;
    justify-content: center;
    align-items: center;
    gap: 8px;
    border-radius: 10px;
    background: #E565A5;
}

.statistics--number {
    color: #FFFBFC;
    text-align: center;
    font-family: Roboto;
    font-size: 12px;
    font-style: normal;
    font-weight: 400;
    line-height: 150%;
    letter-spacing: 0.5px;
}
</style>
