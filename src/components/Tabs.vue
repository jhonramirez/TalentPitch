<script>
import Profile from './Profile.vue'
import Vacancies from './Vacancies.vue'

const routes = {
    '/profile': Profile,
    '/vacancies': Vacancies
}

export default {
    data() {
        return {
            currentPath: window.location.hash
        }
    },
    computed: {
        currentView() {
            return routes[this.currentPath.slice(1) || '#/profile']
        }
    },
    mounted() {
        window.addEventListener('hashchange', () => {
            this.currentPath = window.location.hash
        })
    }
}
</script>
<template>
    <section class="tabs">
        <tab :selected="true">
            <a href="#/profile">Perfil</a>
        </tab>
        <tab>
            <a href="#/vacancies">Vacantes</a>
        </tab>
        <tab>
            <a>Listas</a>
        </tab>
    </section>
    <component :is="currentView" />
</template>

<style scoped>
.tabs {
    display: flex;
    position: relative;
    width: 806px;
    left: 115px;
    height: 52px;
    align-items: flex-end;
    border-bottom: 1px solid #E8EAF6;
}

tab {
    display: flex;
    padding: 16px;
    flex-direction: column;
    justify-content: flex-end;
    align-items: center;
    gap: 10px;
}

a {
    color: #9FA8DA;
    font-family: Inter;
    font-size: 13px;
    font-style: normal;
    font-weight: 600;
    line-height: 150%;
    letter-spacing: 0.5px;
    cursor: pointer;
    text-decoration: none;
}

a:hover {
    color: #DE1C7D;
    text-decoration: underline;
}
</style>
