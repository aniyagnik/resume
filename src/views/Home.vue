<template>
  <div id='home'>
    <h1>This is Home Page</h1>
    <box-container :data=info></box-container>
  </div>
</template>

<script>
import box from '../components/box'

export default {
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
}
</style>
