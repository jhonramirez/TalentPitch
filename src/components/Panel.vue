<script setup>
import PanelLogo from './PanelLogo.vue'
import PanelInfo from './PanelInfo.vue'
import Button from './Button.vue';
import PanelStatisticsItems from './PanelStatisticsItems.vue'
import ShareIcon from './icons/IconShare.vue'
import Download from './download.vue'
</script>

<template>
    <section class="panel">
        <PanelLogo />
        <PanelInfo />
        <img alt="TalentPitch foto" class="foto" src="../assets/foto.svg" />
        <article class="panel--qr">
            <img alt="TalentPitch QR" class="QR" src="../assets/QR.svg" />
        </article>
        <Button label="Compartir perfil" class="panel--button">
            <ShareIcon />
        </Button>
        <Download />
        <PanelStatisticsItems
            :options="[{ title: 'Talentos', number: '20', icon: 'home' }, { title: 'vistas del perfil', number: '20' }, { title: 'Pitches recibidos', number: '20' }, { title: 'Exhibiciones', number: '20' }, { title: 'Vacantes', number: '20' }, { title: 'Contenidos', number: '20' },]" />
    </section>
</template>

<style scoped>
.panel {
    display: flex;
    position: relative;
    max-width: 336px;
    padding: 32px 24px 16px 24px;
    flex-direction: column;
    align-items: center;
    gap: 16px;
    border-radius: 10px;
    border: 1px solid #E8EAF6;
    background: #FFF;
    z-index: 1;
    top: -7vw;
    left: 100px;
}

img {
    display: flex;
    width: 100%;
    height: auto;
    justify-content: center;
    align-items: center;
    gap: 10px;
    align-self: stretch;
    border-radius: 10px;
}

.panel--button{
    width: 100%;
}

.panel--qr {
    display: flex;
    padding: 18px 28px;
    justify-content: center;
    align-items: flex-start;
    gap: 10px;
    align-self: stretch;
    border-radius: 10px;
    border: 1px solid #E8EAF6;
    background: #FFF;
}
</style>
