<template>
  <div id='home'>
    <div class='flex-itemH pic'>
      <img class='pic' src="../assets/1.png" >
    </div>
    <div class='flex-itemH infoBox'>
      <box-container :data='info[0]' :key='info.heading'></box-container>
    </div>
    <div class="flex-itemH" style='padding:2vw;padding-bottom:1vw;flex-grow:4'>
      <div class="flex-inside">
        <div v-for='websiteLink in info[1].websiteLinks' :key='websiteLink.name'>
          <websiteLink-box-container :websiteLink="websiteLink"></websiteLink-box-container>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
import box from '../components/box.vue'
import websiteLinkBox from '../components/websiteLinkBox.vue'

export default {
  name: 'home',
  components: {
    'box-container': box,
    'websiteLink-box-container': websiteLinkBox
  },
  data () {
    return {
      info: [
        {
          heading: 'hi there!',
          title: 'My name is Anirudh Shankar Yagnik',
          summary: ['I have completed Computer Science Engineering from (GGSIPU) with a CGPA of 8.42. ', 'I am experienced with Data Structure, Algorithms and Web design, MERN stack etc.', 'Previously worked at Minds2Mentor as a frontend/backend developer intern.']
        },
        {
          websiteLinks: [
            {
              name: 'github',
              link: 'https://github.com/aniyagnik',
              icon: 'mdi-github'
            },
            {
              name: 'linkedIn',
              link: 'http://linkedin/ani789yagnik',
              icon: 'mdi-linkedin'
            },
            {
              name: 'HackerRank',
              link: 'https://www.hackerrank.com/Ani789yagnik?h_r=internal-search&hr_r=1',
              icon: 'mdi-alpha-h-box'
            }
          ]
        }
      ]
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
    border-radius: 50%;
    box-shadow: 0px 5px 20px rgb(233, 190, 190);
    padding:0vw;
  }
  .pic:hover{
    box-shadow: 0px 3px 20px rgb(194, 17, 17);
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
