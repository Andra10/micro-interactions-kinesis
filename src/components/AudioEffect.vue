<template>
  <kinesis-container class="parent" :audio="audioFile" :playAudio="isPlaying">
    <button
      class="button"
      :class="isPlaying && 'button--playing'"
      @click="changeState"
    />
    <kinesis-audio class="child" type="scale" :strength="75" :audioIndex="70" />
  </kinesis-container>
</template>

<script>
export default {
  data() {
    return {
      audioFile: "audio/area_51.mp3",
      isPlaying: false,
    };
  },
  components: {
    KinesisContainer,
    KinesisElement,
  },
  methods: {
    changeState() {
      this.isPlaying = !this.isPlaying;
    },
  },
};
</script>

<style scoped>
.parent {
  width: 100vw;
  height: 100vh;
  position: relative;
}
.child {
  width: 200px;
  height: 200px;
  background-color: red;
  position: absolute;
  top: calc(50vh - 100px);
  left: calc(50vw - 100px);
}
.button {
  width: 75px;
  height: 75px;
  background-color: gray;
  border-radius: 50%;
  position: absolute;
  top: 25%;
  left: 25%;
}
.button::before,
.button::after {
  content: '';
  position: absolute;
  top: 50%;
  left: 50%;
  transform: translate(-50%, -50%);
}

.button::before {
  width: 30px;
  height: 30px;
  display: none;
  background-color: white;
}
.button::after {
  border-top: 20px solid transparent;
  border-bottom: 20px solid transparent;
  border-left: 20px solid white;
}
.button.button--playing::before {
  display: block;
}
.button.button--playing::after {
  display: none;
}
</style>
