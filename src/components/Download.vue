<script setup>
import DownloadIcon from './icons/IconDownload.vue'
</script>

<template>
    <section class="download">
        <section class="download--content">
            <i>
                <DownloadIcon />
            </i>
            <label>
                <p>Descargar resumen</p>
            </label>
        </section>
    </section>
</template>

<style scoped>
.download {
    display: flex;
    flex-direction: column;
    align-items: flex-start;
    gap: 8px;
    align-self: stretch;  
}

.download--content {
    display: flex;
    align-items: center;
    align-self: stretch;
    border-radius: 8px;
    border: 1px solid #E8EAF6;
    cursor: pointer;
}

i {
    display: flex;
    padding: 10px;
    align-items: flex-start;
    gap: 10px;
    border-radius: 8px 0px 0px 8px;
    background: #DE1C7D;
}

label {
    display: flex;
    width: 259px;
    padding: 0px 16px;
    align-items: center;
    gap: 10px;
    align-self: stretch;
    cursor: pointer;
}

p {
    color: #666;
    font-size: 12px;
    font-style: normal;
    font-weight: 400;
    line-height: 150%;
    letter-spacing: 0.5px;
}
</style>
