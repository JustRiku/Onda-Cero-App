<template>
  <div class="player">
    <!-- song details -->
    <div style="display: flex; flex-direction: column;">
    <div class="song_title">Nombre del podcast</div>
    <div class="song_author">Nombre del locutor</div>
    </div>
    <img style="object-fit: cover; width: 105px; height: 105px;" :src="song.cover" alt="cover">

    <!-- control buttons -->
    <div class="controls">
      <button
        class="btn_control playplause"
        @click="playpause">
          <span v-show="!isPlaiying"><img :src="'/play-solid.svg'" alt=""></span>
          <span v-show="isPlaiying"><img :src="'/pause-solid.svg'" alt=""></span>
      </button>
    </div>
    <!-- progress bar -->
    <div class="progress_bar">
      <div
        @click="seek($event)"
        ref="progress"
        class="no_progress">
          <div
            class="progress"
            :style="{'width' : step + '%'}">
          </div>

      </div>
      <div
        class="progress_btn_pos"
        :style="{'width' : step + '%'}">
          <span
            ref="progressbtn"
            id="progressButtonTimer"
            class="progress_btn"></span>
      </div>

    </div>
    <div class="times">
        <div class="start">0:00</div>
        <div class="end">{{song.end}}</div>
    </div>

  </div>
</template>

<script>
import {Howl, Howler} from 'howler';


export default {
  data(){
    return{
      sound: Object,
      isPlaiying: false,
      isLooping: false,
      step: 0,
      song: {
        title: "File example",
        author: "Anonymous",
        cover: "https://picsum.photos/300/300",
        src: "audios/test.mp3",
        start: 0,
        end: 0
      }
    }
  },
  mounted(){
    this.sound = new Howl({
      src: [this.song.src],
      onload: () => {
        this.song.end = `${Math.round(this.sound._duration/60)}:${Math.round(this.sound._duration)}`;
      }
    });
    this.getTiming();
  },
  methods: {
    playpause(){
      if(this.sound.playing()){
        this.sound.pause();
        this.isPlaiying = false;
      }else{
        this.sound.play();
        this.isPlaiying = true;
      }

    },
    getTiming() {
      setInterval(() => {
        this.updateWidth();
      }, 300)
    },
    updateWidth() {
      if (this.sound.playing()) {
        let width = (this.sound.seek() / this.sound._duration) * 100;
        this.step = Math.round(width);
      }
    },

    toggleLoop(){
      this.isLooping = !this.isLooping;
      this.sound._loop = this.isLooping;
      this.sound._sounds[0]._loop = this.isLooping;
    },

    seek(event){
      const progress = this.$refs.progress;
      let porcent =  event.layerX / progress.clientWidth;

      if (this.sound) {
          if (this.sound.playing()) {
            this.sound.pause();
            this.sound.seek(this.sound._duration * porcent);
            this.sound.play();
            this.step = porcent * 100;
          }else{
            this.sound.seek(this.sound._duration * porcent);
            this.step = porcent * 100;
          }
      }
  }
  }
}
</script>

<style lang="postcss">
</style>