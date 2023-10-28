<script setup>
import ProfileTitle from './ProfileTitle.vue';
import CardKnowledge from './CardKnowledge.vue';
import CardKnowledgeLanguage from './CardKnowledgeLanguage.vue';
import InfoCompany from './InfoCompany.vue';
import ProfileLine from './ProfileLine.vue';
import UserIcon from './icons/IconUser.vue'
import BullseyePointerIcon from './icons/IconBullseyePointer.vue'
import HeadSideBrainIcon from './icons/IconHeadSideBrain.vue'
import BrainIcon from './icons/IconBrain.vue'
import PaperclipIcon from './icons/IconPaperclip.vue'
import ToolsIcon from './icons/IconTools.vue'
import LanguageIcon from './icons/IconLanguage.vue'
import ListIcon from './icons/IconList.vue'
import BadgeCheckIcon from './icons/IconBadgeCheck.vue'
import BriefcaseIcon from './icons/IconBriefcase.vue'
import CommentsIcon from './icons/IconComments.vue'
import UsersIcon from './icons/IconUsers1.vue'
</script>

<template>
    <section class="profile">
        <article class="profile--content">
            <section class="company--summary">
                <article class="title--content">
                    <ProfileTitle label="Resumen de la empresa">
                        <UserIcon />
                    </ProfileTitle>
                </article>
                <InfoCompany />
            </section>
            <section class="knowledge--content">
                <CardKnowledge label="Áreas de interés" :options="['Copy', 'Copy', 'Copy']">
                    <BullseyePointerIcon />
                </CardKnowledge>
                <CardKnowledge label="Vacantes sugeridas por AI" :options="['Copy', 'Copy', 'Copy']">
                    <HeadSideBrainIcon />
                </CardKnowledge>
            </section>
        </article>
        <ProfileLine label="Lo que buscamos en el talento" />
        <article class="profile--content">
            <section class="knowledge--content">
                <CardKnowledge label="Conocimientos"
                    :options="['Copy', 'Copy', 'Copy', 'Copy', 'Copy', 'Copy', 'Copy', 'Copy']">
                    <BrainIcon />
                </CardKnowledge>
                <CardKnowledge label="Habilidades"
                    :options="['Copy', 'Copy', 'Copy', 'Copy', 'Copy', 'Copy', 'Copy', 'Copy']">
                    <PaperclipIcon />
                </CardKnowledge>
            </section>
            <section class="knowledge--content">
                <CardKnowledge label="Herramientas"
                    :options="['Copy', 'Copy', 'Copy', 'Copy', 'Copy', 'Copy', 'Copy', 'Copy']">
                    <ToolsIcon />
                </CardKnowledge>
                <CardKnowledgeLanguage label="Idiomas"
                    :options="[{ title: 'Ingles', subtitle: 'Avanzado' }, { title: 'Frances', subtitle: 'Avanzado' }, { title: 'Frances', subtitle: 'Avanzado' }]">
                    <LanguageIcon />
                </CardKnowledgeLanguage>
            </section>
            <section class="knowledge--content">
                <CardKnowledge label="Metodologías" :options="['Copy', 'Copy', 'Copy', 'Copy']">
                    <ListIcon />
                </CardKnowledge>
            </section>
        </article>
        <ProfileLine label="Lo que ofrecemos en la empresa" />
        <article class="profile--content">
            <section class="knowledge--content">
                <CardKnowledge label="Beneficios que ofrecemos"
                    :options="['Copy', 'Copy', 'Copy', 'Copy', 'Copy', 'Copy', 'Copy', 'Copy']">
                    <BadgeCheckIcon />
                </CardKnowledge>
                <CardKnowledge label="Formas de trabajo que ofrecemos"
                    :options="['Copy', 'Copy', 'Copy', 'Copy', 'Copy', 'Copy', 'Copy', 'Copy']">
                    <BriefcaseIcon />
                </CardKnowledge>
            </section>
            <section class="knowledge--content">
                <CardKnowledge label="Cultura que ofrecemos" :options="['Copy', 'Copy', 'Copy', 'Copy']">
                    <CommentsIcon />
                </CardKnowledge>
                <CardKnowledge label="Comunidades" :options="['Copy', 'Copy', 'Copy', 'Copy']">
                    <UsersIcon />
                </CardKnowledge>
            </section>
        </article>
    </section>
</template>

<style scoped>
.profile {
    display: flex;
    position: relative;
    margin: 1rem;
    left: 115px;
    width: 806px;
    flex-direction: column;
    align-items: flex-start;
    gap: 24px;
}

.profile--content {
    display: flex;
    flex-direction: column;
    align-items: flex-start;
    gap: 16px;
    align-self: stretch;
}

.company--summary {
    display: flex;
    padding: 16px;
    flex-direction: column;
    justify-content: flex-end;
    align-items: flex-start;
    gap: 16px;
    border-radius: 10px;
    border: 1px solid #E8EAF6;
}

.knowledge--content {
    display: flex;
    align-items: flex-start;
    gap: 16px;
    align-self: stretch;
}

.title--content {
    display: flex;
    padding-bottom: 0px;
    align-items: center;
    gap: 8px;
    align-self: stretch;
}
</style>
