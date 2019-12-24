<template>
  <div id='home'>
    <box-container :data='info[0]'></box-container>
  </div>
</template>

<script>
import box from '../components/box.vue'

export default {
  name: 'about',
  components: {
    'box-container': box
  },
  data () {
    return {
      info: [
        {
          heading: 'about',
          content: 'I am an undergraduate student pursuing my Bachelor’s Degree in Computer Science engineering from Maharaja Surajmal Institute of Technology (MSIT). I am hardworking and have good time management skills. I believe my fast learning abilities, good listening skills and commitment to succeed makes me an ideal learner.'
        },
        {
          skills: [
            {
              lang: 'HTML',
              skill: ''
            },
            {
              lang: 'SCSS',
              skill: ''
            },
            {
              lang: 'JAVASCRIPT',
              skill: ''
            },
            {
              lang: 'NODE JS (FOR BACKEND)',
              skill: ''
            },
            {
              lang: 'VUE JS (FOR FRONTEND)',
              skill: ''
            },
            {
              lang: 'C++',
              skill: ''
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
#home{
  background-image: url('../assets/28154.jpg');
  background-attachment: fixed;
  background-position: center;
  background-repeat: no-repeat;
  display: flex;
  justify-content: center;
  align-items: center;
  height: 92.5vh;
}
</style>
