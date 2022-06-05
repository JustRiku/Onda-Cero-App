<template>
    <div class="podcast">
        <div class="image-container">
        <img :src="source" alt="" class="podcast-image">
        </div>
        <div class="podcast-text">
            <p class="program">Nombre podcast</p>
            <p>Nombre locutor</p>
        </div>
    </div>
</template>

<script>
export default {
    name: "Podcast",
    props: ["source"]
}
</script>