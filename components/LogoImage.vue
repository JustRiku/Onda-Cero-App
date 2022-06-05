<template>
    <div>
        <img class="logo-img" :src="source" alt="image">
    </div>
</template>

<script>
export default {
    name: "LogoImage",
    props: ["source"]
}
</script>

<style>
</style>