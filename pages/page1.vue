<template>
<body>
    <nav-bar class="nav-bar"/>
    <hero class="hero"/>
    <main class="main-page1">
        <section class="white">
        <h2>Podcast</h2>
        <div class="podcasts">
            <podcast @click="playpause" :source="'/jrl-1.png'" class="item" v-for="(item, page1) in 8" :key="page1" />
        </div>
        <h2>Programas</h2>
        <div class="cards">
            <card @click="playpause" class="card-item" v-for="(item, page1) in 8" :key="page1" />
        </div>
        </section>
        <section class="cat-section">
        <h2>CATEGORÍAS</h2>
        <h3>Deportes</h3>
        <div class="categorias">
            <category-card @click="playpause" class="cat-item" v-for="(item, page1) in 8" :key="page1" />
        </div>
        <h3>Noticias</h3>
        <div class="categorias">
            <category-card @click="playpause" class="cat-item" v-for="(item, page1) in 8" :key="page1" />
        </div>
        <h3>Actualidad</h3>
        <div class="categorias">
            <category-card @click="playpause" class="cat-item" v-for="(item, page1) in 8" :key="page1" />
        </div>
        <h3>Programas para probar</h3>
        <div class="categorias">
            <category-card @click="playpause" class="cat-item" v-for="(item, page1) in 8" :key="page1" />
        </div>
        </section>
    </main>
</body>
</template>

<style>
</style>

<script>
import NavBar from '../components/NavBar.vue';
import Hero from '../components/Hero.vue';
import LogoImageVue from '../components/LogoImage.vue';
import Podcast from '../components/Podcast.vue';
import Card from '../components/Card.vue';
import CategoryCard from '../components/CategoryCard.vue';
export default{
    name: "Page1",
    components: { Hero, NavBar, LogoImageVue, Podcast, Card, CategoryCard }
}
</script>