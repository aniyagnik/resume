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
          image: 'https://img3.goodfon.com/wallpaper/nbig/b/cf/social-media-icons-3d-cubes.jpg',
          summary: 'A SNS (Social Networking Site) with functionalities like sign-up/login, uploading posts, viewing user, web-lock etc.',
          link: 'https://project1-19.herokuapp.com',
          github: 'https://aniyagnik/nodejsproject19.git'
        },
        {
          name: 'quiz',
          image: 'https://wallpaperaccess.com/full/2384073.jpg',
          summary: 'An website offering quiz on differnt topic of the world. The website offers 10 multiple choice questions on selected topic and keeps track of the rght answers.',
          link: 'https://project1-19.herokuapp.com',
          github: 'https://aniyagnik/nodejsproject19.git'
        },
        {
          name: 'chat app',
          image: 'https://images.unsplash.com/photo-1611606063065-ee7946f0787a?ixlib=rb-1.2.1&ixid=MnwxMjA3fDB8MHxzZWFyY2h8MXx8Y2hhdCUyMGFwcHxlbnwwfHwwfHw%3D&w=1000&q=80',
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
