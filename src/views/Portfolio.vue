<template>
  <div id='portfolio'>
    <h1>This is Portfolio Page</h1>
    <div id='flex'>
      <div class="flex-item" v-for='(project,i) in info' :key='i'>
        <project-card :project='project'></project-card>
      </div>
    </div>
  </div>
</template>

<style lang="scss">
#portfolio{
  background-image: url('../assets/28177.jpg');
  background-attachment: fixed;
  background-position: center;
  background-repeat: no-repeat;
}
#flex{
  display: flex;
  flex-direction: row;
  justify-content: center;
  align-items: center;
  flex-wrap: wrap;
  overflow: auto;
}
.flex-item{
  padding: 5vw;
}
</style>

<script>
import projectCard from '../components/projectCard'
export default {
  components: {
    'project-card': projectCard
  },
  data () {
    return {
      info: [
        {
          name: 'Social Networking Site',
          image: 'SNS.jpg',
          summary: 'A SNS (Social Networking Site) with functionalities sign-up/login, uploading posts, viewing user, web-lock etc.',
          link: 'https://project1-19.herokuapp.com',
          github: 'https://aniyagnik/nodejsproject19.git'
        },
        {
          name: 'quiz',
          summary: '',
          link: '',
          github: ''
        },
        {
          name: 'chat app',
          summary: '',
          link: '',
          github: ''
        },
        {
          name: 'cosmos',
          summary: '',
          link: '',
          github: ''
        }
      ]
    }
  }
}
</script>
