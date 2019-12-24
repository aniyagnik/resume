<template>
  <div id='home'>
    <div class='flex-item'>
      <box-container :data='info' :key='info.heading'></box-container>
    </div>
    <div class="flex-item" style='padding:2vw;padding-bottom:1vw;flex-grow:4'>
      <div class="flex-inside">
        <div class="flex-inside-item">
          <v-icon left dark x-large>mdi-github-circle</v-icon>
          <span class='body-1 font-weight-bold text-capitalize'>github</span><br>
        </div>
        <div class="flex-inside-item">
          <v-icon left dark large>mdi-linkedin-box</v-icon>
          <span class='body-1 font-weight-bold text-capitalize'>linkedIn</span><br>
        </div>
        <div class="flex-inside-item">
          <v-icon left dark>mdi-yin-yang</v-icon>
          <span class='body-1 font-weight-bold text-capitalize'>B.tech in CSE</span><br>
          <p class="caption text-center">pursuing curently</p>
        </div>
      </div>
    </div>
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
        summary: 'I am a Student.I am a designer. I build websites on NodeJs. I am a developer.'
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
  flex-wrap: wrap;
  // border:3px solid rgb(0, 255, 0);
  height: 92.5vh;
  .flex-item {
    // border:1px solid red;
    font-family: -apple-system, BlinkMacSystemFont, 'Segoe UI', Roboto, Oxygen, Ubuntu, Cantarell, 'Open Sans', 'Helvetica Neue', sans-serif;
  }
  .flex-inside{
    color:whitesmoke;
    display: flex;
    justify-content: center;
    flex-wrap: wrap;
    align-items: center;
    // border:1px solid rgb(236, 232, 0);
    .flex-inside-item{
        opacity: 0.6;
        // border:1px solid rgb(235, 11, 11);
        padding-left: 4vw;
        padding-right: 4vw;
    }
    .flex-inside-item:hover{
      cursor: pointer;
      opacity:1.1;
    }
  }
}
</style>
