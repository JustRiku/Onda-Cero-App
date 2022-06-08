<template>
    <nav class="nav-comp">
        <nuxt-link to="/"><logo-image class="logo-image" :source="'/onda-cero-logo.png'"/></nuxt-link>
        <ul>
            <li><nuxt-link to="/page1">Podcasts</nuxt-link></li>
            <li><nuxt-link to="/page2">Mi lista</nuxt-link></li>
            <li><nuxt-link to="">Mi cuenta</nuxt-link></li>
            <li><nuxt-link to="">Buscar</nuxt-link></li>
            <li><nuxt-link to="">Notificaciones</nuxt-link></li>
            <li><nuxt-link to="">Ajustes</nuxt-link></li>
        </ul>
    </nav>
</template>

<script>
import LogoImageVue from "./LogoImage.vue";
export default{
    name: "NavBar",
    componets: {LogoImageVue}
}
</script>