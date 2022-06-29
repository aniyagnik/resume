<template>
  <div id='expierence'>
    <div id='flex'>
      <div class="flex-item" v-for='(experience,i) in info' :key='i'>
        <experience-card :experience='experience'></experience-card>
      </div>
    </div>
  </div>
</template>

<style lang="scss">
#expierence{
  background-image: url('../assets/4566.jpg');
  background-attachment: fixed;
  background-position: center;
  background-repeat: no-repeat;
  flex-direction: row;
  padding-top: 2vw;
  display: flex;
  justify-content: center;
  align-items: center;
  flex-wrap: wrap;
  justify-content: space-evenly;
  height: 100vh;
}
</style>

<script>
import experienceCard from '../components/experienceCard'
export default {
  components: {
    'experience-card': experienceCard
  },
  data () {
    return {
      info: [
        {
          companyName: 'MINDS2MENTOR TECHNOLOGY PRIVATE LIMITED',
          location: 'Bengaluru, Karnataka, India',
          image: 'https://media-exp1.licdn.com/dms/image/C560BAQEuPa9jTaT5VQ/company-logo_200_200/0/1600105990535?e=2147483647&v=beta&t=FbETD0D8w8b3MEEq7xo9juUxTah70Wz0TvCdXNCf3fA',
          post: 'Software Development Intern',
          duration: "Sept'19-Nov'19 (3months)",
          certificate: 'https://drive.google.com/file/d/1KkXrwzVUM8z8Uhj-uTKNTzJncuxfPRoM/view?usp=sharing',
          summary: `Contributed in the development on an e-commerce website which manages delivery of various cuisines from different food outlets present/listed in Dubai.
                        1. Authentication service
                        2. User Cart management service
                        3. Administrator UI & Backend privileges

                        Tech Stack 
                        ReactJS, SCSS Typescript
                        Runtime Environment - NODEJS
                        Database - SQL
                        Project Management Tool - JIRA`
        }
      ]
    }
  }
}
</script>
