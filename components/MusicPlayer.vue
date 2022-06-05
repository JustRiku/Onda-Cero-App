<template>
    <div>
        <div class="player" @click="playpause">
        <play-pause :source="'/play-solid.svg'" v-show="!playing"/>
        <play-pause :source="'/pause-solid.svg'" v-show="playing"/>
        {{ post }}
        </div>
    </div>
</template>

<script>

import {Howl, Howler} from 'howler';
import PlayPause from './PlayPause.vue';

export default{
  components: { PlayPause },
    props: ['post'],
    data () {
        return {
            sound: '',
            playing: false
        }
    },
    mounted () {
        this.sound = new Howl({
            src: ['/audios/test.mp3']
        })
    },
    methods: {
        palypause (){
            this.sound.playing() ? this.sound.pause() : this.sound.play();
        }
    }
}

</script>