<template>
    <div class="player">
        <img class="PlayPauseButton" :src="source" alt="playpause">
    </div>
</template>

<script>
export default{
    name: "PlayPause",
    props: ["source"]
}
</script>