<script setup>
import FacebookIcon from './icons/IconFacebook.vue'
import InstagramIcon from './icons/IconInstagram.vue'
import LinkedinIcon from './icons/IconLinkedin.vue'
import TwitterIcon from './icons/IconTwitter.vue'
</script>

<template>
    <article class="socialNetworks--content">
        <FacebookIcon />
        <InstagramIcon />
        <TwitterIcon />
        <LinkedinIcon />
    </article>
</template>

<style scoped>
.socialNetworks--content {
    display: flex;
    justify-content: center;
    align-items: center;
    gap: 8px;
    cursor: pointer;
}
</style>
