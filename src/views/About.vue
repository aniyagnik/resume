<template>
  <div id='about'>
    <div class="flex-itemA black--text aboutInfo">
      <div id='container-box'>
        <p style='font-size: 2.5em' class=' font-weight-black text-uppercase'>{{ info[0].title}}</p>
        <p style='font-size: 1.25em' class='font-weight-bold text-justify'>{{ info[0].content}}</p>
      </div>
    </div>
    <div class='flex-itemA'><br>
      <h1 style='font-size: 2.5em ' class="text-center white--text font-weight-black text-uppercase">skills</h1>
        <div v-for='skill in info[1].skills' :key='skill.lang'>
          <div style='background-color: black;'>{{skill.lang}}</div>
          <skill-container :skill='skill'></skill-container>
        </div>
    </div>
    <div class="flex-itemA" style='padding:2vw;padding-bottom:1vw;flex-grow:4'>
      <div class="flex-inside">
        <div class="flex-inside-item">
          <v-icon left dark>mdi-yin-yang</v-icon>
          <span style='font-size: 2em'  class=' font-weight-bold text-capitalize'>Krishna Nagar, Delhi</span><br>
          <p class="caption text-center">HomeTown</p>
        </div>
        <div class="flex-inside-item">
          <v-icon left dark>mdi-yin-yang</v-icon>
          <span style='font-size: 2em'  class=' font-weight-bold   text-capitalize'>20 Years</span><br>
          <p class="caption text-center">Age</p>
        </div>
        <div class="flex-inside-item">
          <v-icon left dark>mdi-yin-yang</v-icon>
          <span style='font-size: 2em'  class=' font-weight-bold   text-capitalize'>B.tech in CSE</span><br>
          <p class="caption text-center">pursuing curently</p>
        </div>
      </div>
    </div>
  </div>
</template>

<script>

import skill from '../components/skill'
export default {
  name: 'about',
  components: {
    'skill-container': skill
  },
  data () {
    return {
      info: [
        {
          title: 'about',
          content: 'I am currently pursuing my B.Tech Degree in Computer Science engineering from Guru Gobind Singh Indraprastha University (IP University). Smart working and good time management skills are some of my best qualities. I believe my quick learning abilities, good listening skills and commitment to succeed makes me from the crowd. I am looking for oppotunities to enhance my skills.'
        },
        {
          skills: [
            {
              lang: 'HTML',
              skill: '80'
            },
            {
              lang: 'SCSS',
              skill: '67'
            },
            {
              lang: 'JAVASCRIPT',
              skill: '80'
            },
            {
              lang: 'NODE JS',
              skill: '70'
            },
            {
              lang: 'VUE JS',
              skill: '70'
            },
            {
              lang: 'C++',
              skill: '80'
            }
          ]
        }
      ]
    }
  }
}
</script>
<style lang="scss">
#about{
  background-image: url('../assets/28154.jpg');
  background-attachment: fixed;
  background-position: center;
  background-repeat: no-repeat;
  display: flex;
  justify-content: space-evenly;
  flex-wrap: wrap;
  align-items: center;
  // border:1px solid white;
  width: 100vw;
  .flex-itemA{
    color: whitesmoke;
  }
  #container-box{
    background-color: antiquewhite;
    opacity: 0.6;
    padding: 3vw;
  }
  .flex-inside{
    color:whitesmoke;
    display: flex;
    justify-content: space-evenly;
    flex-wrap: wrap;
    align-items: center;
    // border:1px solid rgb(236, 232, 0);
    .flex-inside-item{
      opacity: 0.6;
      // border:1px solid rgb(235, 11, 11);
    }
    .flex-inside-item:hover{
      cursor: pointer;
      opacity:1.1;
    }
  }
}
/*.skillTable{
  background-image: linear-gradient(to right top, #af1e38, #d04f27, #e28200, #e2b600, #cfeb12);
  padding: 1vw;
  border:2vw solid brown;
  box-shadow: 0px 6px 5px white;
}*/
.aboutInfo{
  max-width:50vw
}
@media only screen and (max-width: 1300px) {
  .aboutInfo{
    max-width:70vw
  }
}
</style>
