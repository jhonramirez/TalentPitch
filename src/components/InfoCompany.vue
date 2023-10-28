<template>
    <article class="description--content">
        <h2 class="description--title">Descripción</h2>
        <p class="description">En ac telecom somos expertos en telecomunicaciones con mas de 25 años
            comprobables en el mercado,
            brindando empleo a mas de 321 empleados al rededor de todo el mundo
        </p>
    </article>
    <article class="info--content">
        <section class="info--contact">
            <h2 class="description--title">Correo electrónico</h2>
            <p class="description">ejemplo@ejemplo.com</p>
        </section>
        <section class="info--contact">
            <h2 class="description--title">Número de contacto</h2>
            <p class="description">3005895648</p>
        </section>
    </article>
    <article class="info--content">
        <section class="info--contact">
            <h2 class="description--title">Estados deseados buscados</h2>
            <p class="description">Emprendedor, practicas, primer empleo</p>
        </section>
        <section class="info--contact">
            <h2 class="description--title">Rol más buscado</h2>
            <p class="description">Lider UX</p>
        </section>
    </article>
</template>

<style scoped>
.description--content {
    display: flex;
    flex-direction: column;
    align-items: flex-start;
    gap: 8px;
    align-self: stretch;
}

.description--title {
    color: #212121;
    text-align: center;
    font-family: Inter;
    font-size: 13px;
    font-style: normal;
    font-weight: 600;
    line-height: 150%;
    letter-spacing: 0.5px;
}

.description {
    color: #666;
    font-family: Inter;
    font-size: 12px;
    font-style: normal;
    font-weight: 400;
    line-height: 150%;
    letter-spacing: 0.5px;
}

.info--content {
    display: flex;
    align-items: flex-start;
    gap: 40px;
    align-self: stretch;
}

.info--contact {
    display: flex;
    flex-direction: column;
    align-items: flex-start;
    gap: 8px;
    flex: 1 0 0;
}
</style>
