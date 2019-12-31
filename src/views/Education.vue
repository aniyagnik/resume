<template>
  <div id='education'>
    <table class="edu-box">
      <tr>
        <th>Class/Degree</th>
        <th>Board/university</th>
        <th>Percentage</th>
        <th>year of passing</th>
      </tr>
      <tr v-for='(obj,i) in institutes' :key='i'>
        <td>{{ obj.type }}</td>
        <td>{{ obj.board }}</td>
        <td>{{ obj.marks }}</td>
        <td>{{ obj.year }}</td>
      </tr>
    </table>
  </div>
</template>

<script>

export default {
  name: 'education',
  data () {
    return {
      institutes: [
        {
          type: '10th',
          board: 'CBSE',
          year: '2015',
          marks: '9.5 percentile'
        },
        {
          type: '12th',
          board: 'CBSE',
          year: '2017',
          marks: '93.4 percentage'
        },
        {
          type: 'B.Tech (CSE)',
          board: 'GGSIPU',
          year: 'pursuing',
          marks: '80 percentage'
        }
      ]
    }
  }
}
</script>
<style lang="scss">
#education{
  background-image: url('../assets/28155.jpg');
  background-attachment: fixed;
  background-position: center;
  background-repeat: no-repeat;
  display: flex;
  justify-content: space-evenly;
  align-items: center;
  flex-wrap: wrap;
  height: 92.5vh;
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
