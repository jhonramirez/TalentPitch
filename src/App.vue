<script setup>
import Banner from './components/Banner.vue'
import Header from './components/Header.vue'
import Panel from './components/panel.vue'
import Match from './components/Match.vue'
import Tabs from './components/Tabs.vue'
</script>

<template>
  <Header :options="['Conéctate', 'Mi muros', 'Mis listas', 'Aprende']"></Header>
  <Banner />
  <section class="main">
    <Panel />
    <section>
      <Match />
      <Tabs />
    </section>
  </section>
</template>

<style scoped>
.main {
  display: flex;
}
</style>
