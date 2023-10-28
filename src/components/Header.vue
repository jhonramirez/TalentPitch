<script setup>
import Button from './Button.vue'
import User from './User.vue'
import BellIcon from './icons/IconBell.vue'
import EnvelopeIcon from './icons/IconEnvelope.vue'
import PlusIcon from './icons/IconPlus.vue'
defineProps({
    options: {
        type: Array,
        required: false,
    }
})
</script>

<template>
    <header class="header">
        <img alt="TalentPitch logo" class="logo" src="../assets/logo.svg" width="125" height="125" />
        <section class="navbar">
            <p v-for="option in options">
                {{ option }}
            </p>
        </section>
        <section class="profile--functions">
            <Button label="Comenzar">
                <PlusIcon />
            </Button>
            <EnvelopeIcon class="icon" />
            <BellIcon class="icon" />
            <User class="icon" />
        </section>
    </header>
</template>

<style scoped>
header {
    background-color: #1A237E;
    display: flex;
    flex-direction: column;
    justify-content: space-between;
    align-items: center;
    padding: 0px 141px;
}

p {
    color: aliceblue;
}

p:hover {
    color: #DE1C7D;
}

.icon {
    cursor: pointer;
}

.navbar {
    display: flex;
    flex-direction: column;
    justify-content: center;
    align-items: center;
    gap: 24px;
    cursor: pointer;
    color: black;
}

.profile--functions {
    display: flex;
    justify-content: center;
    align-items: center;
    gap: 25px;
}

@media (min-width: 1100px) {
    header {
        flex-direction: row;
    }

    .navbar {
        flex-direction: row;
    }
}
</style>
