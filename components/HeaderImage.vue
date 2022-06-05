<template>
    <div>
        <img class="headerImage" :src="source" alt="image">
    </div>
</template>

<script>
export default {
    name: "HeaderImage",
    props: ["source"]
}
</script>

<style>
.headerImage{
    width: 100%;
    object-fit: cover;
}
</style>