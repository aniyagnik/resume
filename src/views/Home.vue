<template>
  <div id='home'>
    <div class='flex-itemH pic'>
      <img class='pic' src="../assets/1.jpg" >
    </div>
    <div class='flex-itemH infoBox'>
      <box-container :data='info' :key='info.heading'></box-container>
    </div>
    <div class="flex-itemH" style='padding:2vw;padding-bottom:1vw;flex-grow:4'>
      <div class="flex-inside">
        <div class="flex-inside-item">
          <a href="https://github.com/aniyagnik">
            <v-icon left dark x-large>mdi-github-circle</v-icon>
            <span style='font-size: 1.1em' class='font-weight-bold white--text text-capitalize'> github</span>
          </a>
        </div>
        <div class="flex-inside-item">
          <a href="http://linkedin/ani789yagnik">
            <v-icon left dark large>mdi-linkedin-box</v-icon>
            <span style='font-size: 1.1em' class='font-weight-bold white--text text-capitalize'>linkedIn</span>
          </a>
        </div>
        <div class="flex-inside-item">
          <a href="https://www.hackerrank.com/Ani789yagnik?h_r=internal-search&hr_r=1">
            <v-icon left dark large>mdi-alpha-h-box</v-icon>
            <span style='font-size: 1.1em' class='body-1 font-weight-bold white--text text-capitalize'>HackerRank</span>
          </a>
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
        heading: 'hi there!',
        line1: 'I am Anirudh Shankar Yagnik',
        summary: ['I am a B.Tech student.', 'I am a good web designer and developer.', 'I am see myself as a good explorer and quick learner.']
      }
    }
  }
}
</script>
<style lang="scss">
#home{
  background-image: url('../assets/28154.jpg');
  background-attachment: fixed;
  background-position: center;
  background-repeat: no-repeat;
  flex-direction: row;
  padding-top: 2vw;
  display: flex;
  justify-content: center;
  align-items: center;
  flex-wrap: wrap;
  height: 92.5vh;
  // border:3px solid rgb(0, 255, 0);
  .pic{
    width: 10vw;
    height: 10vw;
    box-shadow: 0px 5px 20px rgb(233, 190, 190);
    padding:0vw;
  }
  .pic:hover{
    box-shadow: 0px 3px 20px rgb(233, 190, 190);
    transform: all 0.5s;
  }
  .flex-itemH {
    margin:2vw;
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
a{
  text-decoration: none;
}
@media only screen and (max-width: 1080px) {
  #home{
    .pic{
      width: 16vw;
      height: 16vw;
    }
    .infoBox{
      width: 75vw;
    }
  }
}

@media only screen and (max-width: 770px) {
  #home{
    .pic{
      width: 16vw;
      height: 16vw;
    }
  }
}

@media only screen and (max-width: 710px) {
  #home{
    .pic{
      width: 19vw;
      height: 19vw;
    }
  }
}
@media only screen and (max-width: 600px) {
  #home{
    .pic{
      width: 23vw;
      height: 23vw;
    }
  }
}

@media only screen and (max-width: 500px) {
  #home{
    .pic{
      width: 27vw;
      height: 27vw;
    }
  }
}

@media only screen and (max-width: 400px) {
  #home{
    .pic{
      width: 30vw;
      height: 30vw;
    }
  }
}

@media only screen and (max-width: 300px) {
  #home{
    .pic{
      width: 40vw;
      height: 40vw;
    }
  }
}
</style>
