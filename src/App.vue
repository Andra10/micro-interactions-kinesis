<template>
 <ScrollDown />
 <HoverEffect />
 <AudioEffect /> 
</template>

<script>
import ScrollDown from './components/ScrollDown.vue';
import HoverEffect from './components/HoverEffect.vue';
import AudioEffect from './components/AudioEffect.vue';

export default {
  name: 'App',
  components: {
    ScrollDown,
    HoverEffect,
    AudioEffect
  }
}
</script>

<style>

</style>
