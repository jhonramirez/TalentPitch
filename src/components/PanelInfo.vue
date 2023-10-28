<script setup>
import MapMarkerIcon from './icons/IconMapMarker.vue'
import LinkIcon from './icons/IconLink.vue'
import PanelStars from './PanelStars.vue'
import PanelSocialNetworks from './PanelSocialNetworks.vue'
</script>

<template>
    <section class="panel--info">
        <h2 class="panel--title">A.C. Telecom</h2>
        <h2 class="panel--subtitle">@ac-telecom</h2>
        <h2 class="panel--description">Startup - tecnología</h2>
        <section class="panel--content">
            <p class="panel--circle"></p>
            <h2 class="panel--state">Empresa activa</h2>
        </section>
        <section class="panel--content">
            <MapMarkerIcon />
            <h2 class="panel--location">Floridablanca - Colombia</h2>
        </section>
        <PanelStars />
        <PanelSocialNetworks />
        <section class="panel--link">
            <LinkIcon />
            <a href="https://www.actelecom.net/telecom" target="_blank">
                <p class="panel--url">https://www.actelecom.net/telecom</p>
            </a>
        </section>
    </section>
</template>

<style scoped>
.panel--info {
    display: flex;
    flex-direction: column;
    gap: 0.5rem;
    text-align: center;
    font-family: Inter;
    font-style: normal;
    line-height: 150%;
    letter-spacing: 0.5px;
}

.panel--title {
    font-size: 24px;
    font-weight: 600;
    line-height: 125%;
    color: #1A237E;
}

.panel--subtitle {
    font-size: 12px;
    font-weight: 400;
    color: #666;
}

.panel--description {
    font-size: 13px;
    font-weight: 600;
    color: #9FA8DA;
}

.panel--circle {
    display: flex;
    max-width: 8px;
    max-width: 8px;
    padding: 4px;
    align-items: center;
    gap: 10px;
    border-radius: 24px;
    background: #8BC34A;
}

.panel--content {
    display: flex;
    justify-content: center;
    align-items: center;
    gap: 4px;
}

.panel--state {
    font-size: 12px;
    font-weight: 400;
    color: #8BC34A;
}

.panel--location {
    font-size: 12px;
    font-weight: 400;
    letter-spacing: 0.5px;
    color: #666666;
}

a {
    text-decoration: none;
}

.panel--link {
    display: flex;
    justify-content: center;
    align-items: center;
    gap: 4px;
    align-self: stretch;
}

.panel--url {
    font-size: 12px;
    font-weight: 400;
    letter-spacing: 0.5px;
    color: #DE1C7D;
    text-decoration: none;
}
</style>
