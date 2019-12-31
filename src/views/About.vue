<template>
  <div id='about'>
    <div class="flex-item black--text" style="max-width:50vw">
      <div id='container-box'>
        <p class='display-2 font-weight-bold text-capitalize '>{{ info[0].title}}</p>
        <p class='title text-justify'>{{ info[0].content}}</p>
      </div>
    </div>
    <div class='flex-item'><br>
      <h1 class="display-2 white--text font-weight-bold text-capitalize">skills</h1>
      <table cellspacing=30 border='1'>
          <tr>
            <td v-for='skill in info[1].skills.slice(0,2)' :key='skill.lang'>
              <skill-container :skill='skill'></skill-container>
            </td>
          </tr>
          <tr>
            <td v-for='skill in info[1].skills.slice(2,4)' :key='skill.lang'>
              <skill-container :skill='skill'></skill-container>
            </td>
          </tr>
          <tr>
            <td v-for='skill in info[1].skills.slice(4,6)' :key='skill.lang'>
              <skill-container :skill='skill'></skill-container>
            </td>
          </tr>
        </table>
    </div>
    <div class="flex-item" style='padding:2vw;padding-bottom:1vw;flex-grow:4'>
      <div class="flex-inside">
        <div class="flex-inside-item">
          <v-icon left dark>mdi-yin-yang</v-icon>
          <span class='display-1 font-weight-bold text-capitalize'>Krishna Nagar, Delhi</span><br>
          <p class="caption text-center">HomeTown</p>
        </div>
        <div class="flex-inside-item">
          <v-icon left dark>mdi-yin-yang</v-icon>
          <span class='display-1 font-weight-bold   text-capitalize'>20 Years</span><br>
          <p class="caption text-center">Age</p>
        </div>
        <div class="flex-inside-item">
          <v-icon left dark>mdi-yin-yang</v-icon>
          <span class='display-1 font-weight-bold   text-capitalize'>B.tech in CSE</span><br>
          <p class="caption text-center">pursuing curently</p>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
import skill from '../components/skill.vue'

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
  .flex-item{
    // border:1px solid cyan;
    color: whitesmoke;
  }
  #container-box{
    background-color: antiquewhite;
    opacity: 0.6;
    padding: 3vw;
    margin:2vw;
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

</style>
