<template>
  <div id='profile'>
    <div class="flex-itemA">
      <div style='font-size: 2em;border-bottom:5px solid crimson' class="white--text text-uppercase">
        <v-icon dark large>mdi-briefcase</v-icon>
        Work Experience
      </div>
      <div class="flex-item" v-for='(experience,i) in info[0].experience' :key='i'>
        <experience-card :experience='experience'></experience-card>
      </div>
    </div>
    <div class='flex-itemA'><br>
      <div style='font-size: 2em;border-bottom:5px solid yellow ' class="white--text text-uppercase">
        <v-icon dark large>mdi-chart-bar</v-icon>
        Skills
      </div>
      <br>
      <div v-for='skill in info[1].skills' :key='skill.lang'>
        <div style='margin-left:5px;'>{{skill.lang}}</div>
        <skill-container :skill='skill'></skill-container>
      </div>
    </div>
    <div class="flex-itemA" >
      <div style='font-size: 2em;border-bottom:5px solid yellow ' class="white--text text-uppercase">
        <v-icon dark large>mdi-book-open-page-variant</v-icon>
        education</div>
      <br>
      <div v-for='(institute,i) in info[2].institutes' :key=i>
        <edu-container :institute='institute'></edu-container>
      </div>
    </div>
    <div class="flex-itemA" style='min-width:100vw;padding:2vw;padding-bottom:1vw;flex-grow:4'>
      <div class="flex-inside">
        <div class="flex-inside-item">
          <v-icon left dark>mdi-yin-yang</v-icon>
          <span style='font-size: 2em'  class=' font-weight-bold text-capitalize'>Krishna Nagar, Delhi</span><br>
          <p class="caption text-center">HomeTown</p>
        </div>
        <div class="flex-inside-item">
          <v-icon left dark>mdi-yin-yang</v-icon>
          <span style='font-size: 2em'  class=' font-weight-bold   text-capitalize'>22 Years</span><br>
          <p class="caption text-center">Age</p>
        </div>
        <div class="flex-inside-item">
          <v-icon left dark>mdi-yin-yang</v-icon>
          <span style='font-size: 2em'  class=' font-weight-bold   text-capitalize'>B.tech in CSE</span><br>
          <p class="caption text-center">2017-21</p>
        </div>
      </div>
    </div>
  </div>
</template>

<script>

import experienceCard from '../components/experienceCard'
import skill from '../components/skill'
import edu from '../components/education'

export default {
  name: 'profile',
  components: {
    'experience-card': experienceCard,
    'skill-container': skill,
    'edu-container': edu
  },
  data () {
    return {
      info: [
        {
          experience: [
            {
              companyName: 'Minds2Mentor',
              companyLink: 'https://www.minds2mentor.com/',
              post: 'Software Development Intern',
              duration: "Sept'19-Nov'19 (3months)",
              certificate: 'https://drive.google.com/file/d/1KkXrwzVUM8z8Uhj-uTKNTzJncuxfPRoM/view?usp=sharing',
              summary: ['Authentication service', 'User Cart management service', 'Administrator UI & Backend privileges']
            }
          ]
        },
        {
          skills: [
            {
              lang: 'HTML/SCSS',
              skill: '80',
              color: 'blue lighten-4'
            },
            {
              lang: 'JAVASCRIPT',
              skill: '80',
              color: 'deep-orange lighten-2'
            },
            {
              lang: 'NODE JS',
              skill: '80',
              color: 'lime accent-2'
            },
            {
              lang: 'Typescript',
              skill: '80',
              color: 'red lighten-5'
            },
            {
              lang: 'ReactJS',
              skill: '70',
              color: 'indigo darken-1'
            },
            {
              lang: 'VUE JS',
              skill: '74',
              color: 'green lighten-2'
            },
            {
              lang: 'C++',
              skill: '84',
              color: 'teal darken-1'
            },
            {
              lang: 'SQL / NO-SQL',
              skill: '75',
              color: 'red lighten-1'
            }
          ]
        },
        {
          institutes: [
            {
              name: 'Maharaja Surajmal Institute Of Technology',
              degree: 'B.Tech (CSE)',
              board: 'GGSIPU',
              year: '2021',
              place: 'delhi',
              marks: '84.2 percentage'
            },
            {
              name: 'Universal Public School',
              degree: '12th',
              board: 'CBSE',
              year: '2017',
              place: 'delhi',
              marks: '93.4 percentage'
            },
            {
              name: 'Universal Public School',
              degree: '10th',
              board: 'CBSE',
              year: '2015',
              place: 'delhi',
              marks: '9.5 percentile'
            }
          ]
        }
      ]
    }
  }
}
</script>
<style lang="scss">
#profile{
  background-image: url('../assets/bg (3).png');
  background-attachment: fixed;
  background-position: center;
  background-repeat: no-repeat;
  display: flex;
  justify-content: space-evenly;
  flex-wrap: wrap;
  align-items: center;
  flex-direction: row;
  width: 100vw;
  .flex-itemA{
    color: whitesmoke;
    padding:10px;
    justify-content: space-evenly;
    flex-direction: row;
    align-items: flex-start;
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
  .edu-box{
      background-image: linear-gradient(to right top, #181517, #363237, #57535a, #797680, #9b9ca9, #9a9fab, #99a1ad, #99a4af, #78848b, #5a6468, #3f4647, #262a2a);
      opacity: 0.9;
      padding: 1vw;
      box-shadow: 0px 6px 20px white;
      color: whitesmoke;
      cursor: pointer;
    }
    .edu-box:active {
        color:red;
        box-shadow: 0px 6px 15px rgb(148, 4, 4);
    }
    tr:nth-child(even) {background-color: #f2f2f2;}
    th {
      background-color: #4CAF50;
      color: white;
    }
    th, td {
      padding: 15px;
      text-align: left;
      color: black;
      }
}

</style>
