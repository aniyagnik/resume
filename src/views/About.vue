<template>
  <div id='about'>
    <div class='flex-item' id='container-box'>
       <p class='display-1 font-weight-bold text-capitalize'>{{ info[0].title}}</p>
       <p class='subtitle-1'>{{ info[0].content}}</p>
   </div>
   <div class='flex-item'>
     <h1 class="display-2 white--text font-weight-bold text-capitalize">skills</h1>
     <table cellspacing=30>
        <tr>
          <td v-for='skill in info[1].skills.slice(0,3)' :key='skill.lang'>
            <skill-container :skill='skill'></skill-container>
          </td>
        </tr>
        <tr>
          <td v-for='skill in info[1].skills.slice(3,7)' :key='skill.lang'>
            <skill-container :skill='skill'></skill-container>
          </td>
        </tr>
      </table>
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
          content: 'I am an undergraduate student pursuing my Bachelor’s Degree in Computer Science engineering from Maharaja Surajmal Institute of Technology (MSIT). I am hardworking and have good time management skills. I believe my fast learning abilities, good listening skills and commitment to succeed makes me an ideal learner.'
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
              lang: 'NODE JS (FOR BACKEND)',
              skill: '70'
            },
            {
              lang: 'VUE JS (FOR FRONTEND)',
              skill: '70'
            },
            {
              lang: 'C++',
              skill: '80'
            }
          ]
        },
        {
          personalInfo: [
            {
              title: 'HomeTown',
              content: 'Krishna Nagar, Delhi'
            },
            {
              title: 'schooling',
              content: 'Universal Public School',
              session: '2017',
              marks1: '9.5',
              marks: '93.5'
            },
            {
              title: 'Graduation',
              content: 'Maharaja Surajmal Institute Of Technology',
              marks1: '8'
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
  justify-content: center;
  align-items: center;
  flex-direction: column;
  width: 100vw;
  #container-box{
    background-color: antiquewhite;
    opacity: 0.6;
    padding: 3vw;
  }
  .flex-item{
    padding-right: 2vh;
  }
}

</style>
