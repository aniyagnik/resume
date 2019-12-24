<template>
  <div id='home'>
    <box-container :data='info' :key='info.heading'></box-container>
  </div>
</template>

<script>
import box from '../components/box.vue'

export default {
  name: 'home',
  components: {
    'box-container': box
  },
  data () {
    return {
      info: {
        heading: 'hi! there',
        line1: 'I am Anirudh Shankar Yagnik',
        content: 'I am a Student.I am a designer. I build websites on developer.'
      }
    }
  }
}
</script>
<style lang="scss">
#home{
  background-image: url('../assets/28171.jpg');
  background-attachment: fixed;
  background-position: center;
  background-repeat: no-repeat;
  display: flex;
  justify-content: center;
  align-items: center;
  height: 92.5vh;
}
</style>
