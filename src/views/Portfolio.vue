<template>
  <div id='portfolio'><br>
    <div style='text-align:center;font-size:2em;color:white;font-weight:800'>MY PORTFOLIO</div>
    <div id='flex'>
      <div class="flex-item" v-for='(project,i) in info' :key='i'>
        <project-card :project='project'></project-card>
      </div>
    </div>
  </div>
</template>

<style lang="scss">
#portfolio{
  background-image: url('../assets/Computer-Tech.jpg');
  background-attachment: fixed;
  background-position: center;
  background-repeat: no-repeat;
}
#flex{
  display: flex;
  flex-direction: row;
  justify-content: center;
  align-items: center;
  overflow: auto;
  flex-wrap: wrap;
}
@media only screen and (min-width: 1000px) {
  .flex-item{
    padding: 5vw;
  }
}
.flex-item{
    padding: 3vw;
  }
@media only screen and (max-width: 850px) {
  .flex-item{
    padding-right: 1vw;
    padding-left: 1vw;
  }
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
          image: 'https://wallpaperplay.com/walls/full/c/1/7/215281.jpg',
          summary: 'A SNS (Social Networking Site) with functionalities like sign-up/login, uploading posts, viewing user, web-lock etc.',
          link: 'https://project1-19.herokuapp.com',
          github: 'https://aniyagnik/nodejsproject19.git'
        },
        {
          name: 'quiz',
          image: 'https://www.ecopetit.cat/wpic/mpic/81-817751_quiz-time-announcement-poster-neon-signboard-vector-quiz.jpg',
          summary: 'An website offering quiz on differnt topic of the world. The website offers 10 multiple choice questions on selected topic and keeps track of the rght answers.',
          link: 'https://project1-19.herokuapp.com',
          github: 'https://aniyagnik/nodejsproject19.git'
        },
        {
          name: 'chat app',
          image: 'https://clip.cookdiary.net/sites/default/files/wallpaper/comics-clipart/424345/comics-clipart-message-box-424345-6923408.jpg',
          summary: 'Offers to chat with friends on login is performed. Can send messages to multiple users at a given time. offers option of personal chat.',
          link: 'https://project1-19.herokuapp.com',
          github: 'https://aniyagnik/nodejsproject19.git'
        },
        {
          name: 'cosmos',
          image: 'https://wallpaperaccess.com/full/19922.jpg',
          summary: 'Website give interesting information about the cosmos. Detailed discription of our solar system.',
          link: 'https://project1-19.herokuapp.com',
          github: 'https://aniyagnik/nodejsproject19.git'
        }
      ]
    }
  }
}
</script>
