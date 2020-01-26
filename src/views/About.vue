<template>
  <div id='about'>
    <div class="flex-itemA black--text aboutInfo">
      <div id='container-box'>
        <p style='font-size: 2.5em' class=' font-weight-black text-uppercase'>{{ info[0].title}}</p>
        <p style='font-size: 1.25em' class='font-weight-bold text-justify'>{{ info[0].content}}</p>
      </div>
    </div>
    <div class='flex-itemA'><br>
      <div style='font-size: 2em;border-bottom:5px solid yellow ' class="white--text text-uppercase">
        <v-icon dark large>mdi-chart-bar</v-icon>
        skills</div>
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
    <div class='flex-itemA'><br>
      <div style='font-size: 2em;border-bottom:5px solid yellow ' class="white--text text-uppercase">
        <v-icon dark large>mdi-alphabetical</v-icon>
        Languages</div>
        <br>
        <div v-for='skill in info[3].languages' :key='skill.lang'>
          <div style='margin-left:5px;'>{{skill.lang}}</div>
          <skill-container :skill='skill'></skill-container>
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
import edu from '../components/education'
export default {
  name: 'about',
  components: {
    'skill-container': skill,
    'edu-container': edu
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
              skill: '80',
              color: 'blue lighten-4'
            },
            {
              lang: 'SCSS',
              skill: '67',
              color: 'indigo darken-1'
            },
            {
              lang: 'JAVASCRIPT',
              skill: '80',
              color: 'deep-orange lighten-2'
            },
            {
              lang: 'NODE JS',
              skill: '70',
              color: 'lime accent-2'
            },
            {
              lang: 'VUE JS',
              skill: '70',
              color: 'green lighten-2'
            },
            {
              lang: 'C++',
              skill: '80',
              color: 'teal darken-1'
            }
          ]
        },
        {
          institutes: [
            {
              name: 'Universal Public School',
              degree: '10th',
              board: 'CBSE',
              year: '2015',
              place: 'delhi',
              marks: '9.5 percentile'
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
              name: 'Maharaja Surajmal Institute Of Technology',
              degree: 'B.Tech (CSE)',
              board: 'GGSIPU',
              year: 'pursuing',
              place: 'delhi',
              marks: '80 percentage'
            }
          ]
        },
        {
          languages: [
            {
              lang: 'Hindi',
              skill: '90',
              color: 'orange'
            },
            {
              lang: 'English',
              skill: '70',
              color: 'blue'
            },
            {
              lang: 'Gujarati',
              skill: '70',
              color: 'yellow'
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
  //border:10px solid white;
  width: 100vw;
  .flex-itemA{
    color: whitesmoke;
    padding:10px;
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
