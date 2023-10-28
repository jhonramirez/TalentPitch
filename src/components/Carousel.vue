<script>
import 'vue3-carousel/dist/carousel.css'
import { Carousel, Slide, Navigation } from 'vue3-carousel'
import axios from "axios"
import Card from './Card.vue'
const url = "https://data2.talentpitch.co/api/homeservice/categories/d/challenges/trending_challenges/unique/null?limit=10"
export default {
    name: 'App',
    data() {
        return {
            info: null
        }
    },
    mounted() {
        axios
            .get(url)
            .then(response => (this.info = response.data.data))
    },
    components: {
        Carousel,
        Slide,
        Card,
        Navigation,
    },
}
</script>
<template>
    <p class="carousel--title">Publicadas recientemente</p>
    <carousel :items-to-show="2.8" class="carousel">
        <slide v-for="infoCard in  info " :key="slide" class="slider">
            <Card :infoCard="infoCard" />
        </slide>
        <template #addons>
            <navigation />
        </template>
    </carousel>
</template>

<style scoped>
.carousel--title {
    position: relative;
    left: 115px;
    color: #1A237E;
    font-family: Roboto;
    font-size: 24px;
    font-style: normal;
    font-weight: 500;
    line-height: 125%;
    letter-spacing: 0.5px;
    padding: 2rem 0 1rem 0;
}

.carousel {
    max-width: 806px;
    left: 115px;
    padding: 16px 0px;
}

.slider {
    display: flex;
    align-items: flex-end;
    gap: 16px;
    flex: 1 0 0;
}
</style>
